# 列表渲染

###ux:for

在组件上使用 ```ux:for``` 控制属性绑定一个数组，即可使用数组中各项的数据重复渲染该组件。

默认数组的当前项的下标变量名默认为 index，数组当前项的变量名默认为 item

```
<view ux:for="{{array}}">
  {{index}}: {{item.message}}
</view>
```

```
Component({
  data: {
    array: [{
      message: 'foo',
    }, {
      message: 'bar'
    }]
  }
})
```

使用 ux:for-item 可以指定数组当前元素的变量名，

使用 ux:for-index 可以指定数组当前下标的变量名：


```
<view ux:for="{{array}}" ux:for-index="idx" ux:for-item="itemName">
  {{idx}}: {{itemName.message}}
</view>
```

**注意:**

当 ```ux:for``` 的值为字符串时，会将字符串解析成字符串数组

```
<view ux:for="array">
  {{item}}
</view>
```

等同于

```
<view ux:for="{{['a','r','r','a','y']}}">
  {{item}}
</view>
```