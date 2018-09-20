#网络
## 发起请求
###ux.request(OBJECT)
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
ux.request({
  url:'https://wechat.xin.com/worldcup/tools/get_data',
  data:'',
  method:'GET'
}).then((res)=>{
      console.log(res)
})
  
```



##上传下载

敬请期待

##数据储存
  wx: setStorage  setStorageSync  getStorage  getStorageSync 

  bd: setStorage  setStorageSync  getStorage  getStorageSync 

  qk: Storage.set  storage.clear  Storage.get Storage.clear(删除所有) Storage.delete(删除部分)





##获取位置




##查看位置



##拨打电话



##交互反馈