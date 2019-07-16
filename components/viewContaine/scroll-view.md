# scroll-view
可滚动视图区域。

**属性及支持度**

属性|类型|默认值|说明|微信|百度|快应用|字节跳动
---|---|---|---|---|---|---
scroll-x | Boolean | false | 允许横向滚动 | ✔️ | ✔️  | Ｘ | ✔️
scroll-y | Boolean | false | 允许纵向滚动 | ✔️ | ✔️ | Ｘ | ✔️
upper-threshold | Number | 50 | 距顶部/左边多远时（单位px），触发 scrolltoupper 事件 | ✔️ | ✔️ | Ｘ | ✔️
lower-threshold | Number | 50 | 距底部/右边多远时（单位px），触发 scrolltolower 事件 | ✔️ | ✔️ | Ｘ | ✔️
scroll-top | Number |  | 设置竖向滚动条位置 | ✔️ | ✔️ | Ｘ | ✔️
scroll-left | Number |  | 设置横向滚动条位置 | ✔️ | ✔️ | Ｘ | ✔️
scroll-into-view | String |  | 值应为某子元素id（id不能以数字开头）。设置哪个方向可滚动，则在哪个方向滚动到该元素 |✔️ | ✔️ | Ｘ | ✔️
scroll-with-animation | Boolean | false | 在设置滚动条位置时使用动画过渡 | ✔️ | ✔️ | Ｘ | ✔️
enable-back-to-top | Boolean | false | iOS点击顶部状态栏、安卓双击标题栏时，滚动条返回顶部，只支持竖向 | ✔️ | Ｘ | Ｘ | X
bindscrolltoupper | EventHandle |  | 滚动到顶部/左边，会触发 scrolltoupper 事件 | ✔️  | ✔️ | ✔️ | ✔️
bindscrolltolower | EventHandle |  | 滚动到底部/右边，会触发 scrolltolower 事件 | ✔️ | ✔️ | ✔️ | ✔️
bindscroll | EventHandle |  | 滚动时触发，event.detail = {scrollLeft, scrollTop, scrollHeight, scrollWidth, deltaX, deltaY} | ✔️ | ✔️ | ✔️ | ✔️
scrollpage | Boolean | false | 是否将list顶部页面中非list部分随list一起滑出可视区域，开启该属性会降低list渲染性能 | Ｘ | Ｘ | ✔️ | X
