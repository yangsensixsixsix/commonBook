# view
视图容器。

**属性及支持度**

属性|类型|默认值|说明|微信|百度|快应用|字节跳动
---|---|---|---|---|---|---
hover-class | String | none | 指定按下去的样式类。当 hover-class="none" 时，没有点击态效果 | ✔️ | ✔️ | Ｘ | ✔️
hover-stop-propagation | Boolean | false | 指定是否阻止本节点的祖先节点出现点击态 | ✔️ | ✔️ | Ｘ | ✔️ 
hover-start-time | Number | 50 | 按住后多久出现点击态，单位毫秒 | ✔️ | ✔️ | Ｘ | ✔️ 
hover-stay-time | Number | 400 | 手指松开后点击态保留时间，单位毫秒 | ✔️ | ✔️ | Ｘ | ✔️ 

**示例**

```
<view class="single-text-area">
    <view class="view-more">
        <text>点击加载更多</text>
    </view>
</view>
```