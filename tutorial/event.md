##事件处理

**通用方案** 事件绑定属性采用驼峰式命名法，写法很简单，和小程序的一致。举个栗子：

```
    <view bindtap="Event">
        clickMe
    </view>
```

##向事件处理程序传递参数

通常我们会为事件处理程序传递额外的参数。例如，若是 carid 是你要使用的 carid，应使用以下方式向事件处理程序传递参数：

```

    <button bindtap="eventHandler" data-carid="2392" data-cityid="201">Something</button>

```
在JS中从该函数接收的事件对象e里可以拿到该参数

```
Component ({
    methods:{
        eventHandler:function(e){
            console.log(e.currentTarget.dataset.carid);//2392
        }
    }
})
```
**注意要用currentTarget.dataset，不要用target.dataset**




