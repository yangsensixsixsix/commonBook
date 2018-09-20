# 条件渲染
###ux:if
在 **通用方案** 中，条件渲染的写法和微信小程序中基本一致，使用操作符ux:if来决定改元素是否显示：

```
<view ux:if="{{condition}}"> True</view>

```
以上代码中，我们通过condition作为参数来判定view组件是否显示，当condition为true时显示，反之则隐藏。