# 教程

## 项目目录结构
```
├── bin                   编译工具目录
|   ├── common            编译方法目录
|   |   ├── api           api处理目录
|   |   └── components    组件处理目录
|   └── compileApi.js     编译入口文件            
├── debug                 组件调试目录
|   ├── wx_workspace      微信调试目录
|   ├── bd_workspace      百度调试目录
|   └── qk_workspace      快应用调试目录
├── dist                  组件生成目录
|   ├── wx                微信生成目录
|   ├── bd                百度生成目录
|   └── qk                快应用生成目录
└── components            组件开发目录  


```


#页面
**通用方案** 项目中的每个组件开发时应在`components`目录下创建一个属于自己独立的目录,如`index`文件夹，包含`index.js`、`index.css`和`index.html`。

**代码示例** 

```
Component ({
    properties:{
      myProperty:{
          type:String,
          value:'ahaha',
          observer:function(newVal,oldVal){
              //监听函数，当myProperty发生变化时触发
              console.log("myProperty has changed")
          }
      }
    },
    data:{},//私有数据，用于模板渲染
    attached:function(){},//组件生命周期函数，在组件实例进入页面节点树时执行 
    ready:function(){},//组件生命周期函数，在组件布局完成后执行，此时可以获取节点信息
    detached:function(){},//组件生命周期函数，在组件实例被从页面节点树移除时执行 
    methods:{
        eventName:function(){
            console.log("我是event");
        }
    }
}) 
```


**生命周期** 

生命周期方法|说明|作用
---|---|---
attached | 组件实例进入页面 |可以在此请求后台接口 
ready | 组件布局完成 |
detached | 组件实例被从页面节点树移除 |

此外，在微信小程序中还有如下生命周期：

生命周期方法|说明
---|---|---
moved | 组件实例被移动到节点树另一个位置 
created | 组件实例进入页面节点树时执行，注意此时不能调用 setData

以上周期函数 目前只有微信小程序端支持，编译到快应用和百度小程序端会失效。