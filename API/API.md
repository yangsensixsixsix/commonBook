
## 更新视图
###ux.setData(OBJECT)

会把data或properties中的数据进行赋值，并更新页面。

参数  | 类型 | 必填 | 默认值 | 说明
---|---|---|---|---
data | Object | 是 |  | 需要更新的数据（群组）
pointer |  | 是 |   | this
cb | FUNCTION | 否 |  | 回调函数，会在页面更新完后调用

#网络
## 发起请求
###ux.request(OBJECT)
发起网络请求

**OBJECT 参数说明：**

参数  | 类型 | 必填 | 默认值 | 说明
---|---|---|---|---
url | String | 是 |  | 开发者服务器接口地址
data | Object/String/ArrayBuffer | 否 |   | 请求的参数
header | Object | 否 |  | 设置请求的 header，header 中不能设置 Referer
method | String | 否 | GET | （需大写）有效值：OPTIONS, GET, HEAD, POST, PUT, DELETE, TRACE, CONNECT


###appFetch(OBJECT)
发起网络请求，**须 `Promise` 化使用。**

**OBJECT 参数说明：**

参数  | 类型 | 必填 | 默认值 | 说明
---|---|---|---|---
url | String | 是 |  | 开发者服务器接口地址
data | Object/String/ArrayBuffer | 否 |   | 请求的参数
header | Object | 否 |  | 设置请求的 header，header 中不能设置 Referer
method | String | 否 | GET | （需大写）有效值：OPTIONS, GET, HEAD, POST, PUT, DELETE, TRACE, CONNECT

**成功返回参数说明：**

参数 | 类型 | 说明
---|---|---
data | Object/String | 开发者服务器返回的数据
code | Number | 开发者服务器返回的 HTTP 状态码
message | String | 开发者服务器返回的 message


**示例代码**

```
appFetch({
  url:'https://wechat.xin.com/worldcup/tools/get_data',
  data:'',
  method:'GET'
}).then((res)=>{
    console.log(res)
})

```


## 上传下载

敬请期待

## 数据缓存
###ux.setStorage(OBJECT)

修改存储内容

**OBJECT 参数说明：**

参数  | 类型 | 必填 | 说明
---|---|---|---
key | String | 是 | 本地缓存中指定的 key
data | String/Object/Array | 否 | 需要存储的内容
success | Function | 否 | 接口调用成功的回调函数
fail | Function | 否 | 接口调用失败的回调函数
complete | Function | 否 | 接口调用结束的回调函数（调用成功、失败都会执行）

###ux.getStorage(OBJECT)

从本地缓存中异步获取指定 key 的内容

**OBJECT 参数说明：**

参数  | 类型 | 必填 | 说明
---|---|---|---
key | String | 是 | 本地缓存中指定的 key
success | Function | 否 | 接口调用成功的回调函数
fail | Function | 否 | 接口调用失败的回调函数
complete | Function | 否 | 接口调用结束的回调函数（调用成功、失败都会执行）


###ux.clearStorage(OBJECT)

清理本地数据缓存

**OBJECT 参数说明：**

参数  | 类型 | 必填 | 说明
---|---|---|---
success | Function | 否 | 接口调用成功的回调函数
fail | Function | 否 | 接口调用失败的回调函数
complete | Function | 否 | 接口调用结束的回调函数（调用成功、失败都会执行）


###ux.removeStorage(OBJECT)

从本地缓存中移除指定 key

**OBJECT 参数说明：**

参数  | 类型 | 必填 | 说明
---|---|---|---
key | String | 是 | 本地缓存中指定的 key
success | Function | 否 | 接口调用成功的回调函数
fail | Function | 否 | 接口调用失败的回调函数
complete | Function | 否 | 接口调用结束的回调函数（调用成功、失败都会执行）

<!-- 
  wx: (setStorage  setStorageSync)  (getStorage  getStorageSync)   (clearStorage   clearStorageSync)  (removeStorage  removeStorageSync)

  bd: (setStorage  setStorageSync)  (getStorage  getStorageSync)   (clearStorage   clearStorageSync)  (removeStorage  removeStorageSync)

  qk:        storage.set                   storage.get                     storage.clear(删除所有)          storage.delete(删除部分)
 -->

##获取位置

敬请期待


##查看位置

敬请期待

##拨打电话

敬请期待

##交互反馈
###ux.showToast(OBJECT)

显示消息提示框

**OBJECT 参数说明：**

参数  | 类型 | 必填 | 默认值 | 说明 | 微信|百度|快应用
---|
title | string | 否 |  | 提示的内容 |✔️ | ✔️|✔️
icon | string | 否 | 'success' | 图标 |✔️ |✔️ |X
image | string | 否 |  | 自定义图标的本地路径，image 的优先级高于 icon |✔️ | ✔️| X
duration | number | 1500 | 否 | 提示的延迟时间 |✔️ |✔️ |✔️
mask | boolean | false | 否 | 是否显示透明蒙层，防止触摸穿透 |✔️ | ✔️|X
success | function |  | 否 | 接口调用成功的回调函数 | ✔️| ✔️|X
fail | function |  | 否 | 接口调用失败的回调函数 | ✔️|✔️ |X
complete | function |  | 否 | 接口调用结束的回调函数（调用成功、失败都会执行）|✔️ | ✔️|X


## 导航
###ux.navigateTo(OBJECT)
保留当前页面，跳转到应用内的某个页面，但是不能跳到 tabbar 页面。使用 ux.navigateBack 可以返回到原页面。

**OBJECT 参数说明：**

参数  | 类型 | 必填 | 默认值 | 说明 | 微信|百度|快应用
---|
url | string | 是 |  | 需要跳转的应用内非 tabBar 的页面的路径, 路径后可以带参数。参数与路径之间使用 ? 分隔，参数键与参数值用 = 相连，不同参数用 & 分隔；如 'path?key=value&key2=value2' |✔️ | ✔️|✔️
success | function | 否 |  | 接口调用成功的回调函数 |✔️ |✔️ |X
fail | function | 否 |  | 接口调用失败的回调函数 |✔️ | ✔️| X
complete | function | 否 |  | 接口调用结束的回调函数（调用成功、失败都会执行） |✔️ |✔️ |X

###ux.redirectTo(OBJECT)
关闭当前页面，跳转到应用内的某个页面，但是不允许跳转到 tabbar 页面。

使用方法同`ux.navigateTo`。

###ux.navigateBack(OBJECT);
关闭当前页面，返回上一页面或多级页面。

参数  | 类型 | 必填 | 默认值 | 说明 | 微信|百度|快应用
---|
delta | number | 是 |  | 返回的页面数，如果 delta 大于现有页面数，则返回到首页。 |✔️ | ✔️|✔️
success | function | 否 |  | 接口调用成功的回调函数 |✔️ |✔️ |X
fail | function | 否 |  | 接口调用失败的回调函数 |✔️ | ✔️| X
complete | function | 否 |  | 接口调用结束的回调函数（调用成功、失败都会执行） |✔️ |✔️ |X


## 滑块

###ux.swiperTo(OBJECT)

用于控制swiper组件内滑块的滑动。

参数  | 类型 | 必填 | 默认值 | 说明 
---|
pointer | this | 是 |  | 当前页面的指针 
id | string | 是 |  | 需要滑动的swiper的id 
index | string | 是 |  | 需要跳到的图片索引 
indexName | string | 是 |  | 控制索引的变量名称 


## 组件通信

###ux.dispatch(OBJECT)

父子组件之间的通信中，用于子组件接受父组件传来的方法。

参数  | 类型 | 必填 | 默认值 | 说明 
---|
pointer | this | 是 |  | 当前页面的指针
sign | string | 是 |  | 所传递方法的标志符
data | string | 是 |  | 需要传递的参数

**示例代码**

```
//子组件
<view bindtap="click"></view>

Component({
    method(){
        click:function(){
            ux.dispatch({
                pointer:this,
                sign:'eventSign',
                data:{
                    param
                }
            })
        }
    }
})
```