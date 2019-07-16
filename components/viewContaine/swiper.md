# scroll
滑块视图容器。

**属性及支持度**

属性|类型|默认值|说明|微信|百度|快应用|字节跳动
---|---|---|---|---|---|---
indicator-dots | Boolean | false | 是否显示面板指示点 | ✔️ | ✔️ | ✔️ | ✔️
indicator-color | Color | rgba(0, 0, 0, .3) | 指示点颜色	 | ✔️ | ✔️ | ✔️ | ✔️
indicator-size | String | "20px" | 面板指示点的直径大小 | X | X | ✔️ | X
indicator-active-color | Color | #000000 | 当前选中的指示点颜色件	 | ✔️ | ✔️ | ✔️ | ✔️
autoplay | Boolean | false | 是否自动切换	 | ✔️ | ✔️ | ✔️ | ✔️
current | Number | 0 | 当前所在页面的 index	 | ✔️ | ✔️ | ✔️ | ✔️
current-item-id | String | "" | 当前所在滑块的 item-id ，不能与 current 被同时指定 | ✔️ | ✔️ | Ｘ | ✔️
interval | Number | 5000 | 自动切换时间间隔	 |✔️ | ✔️ | ✔️ | ✔️
duration | Number | 500 | 滑动动画时长	 | ✔️ | ✔️ | Ｘ | ✔️
circular | Boolean | false | 是否采用衔接滑动	 | ✔️ | ✔️ | ✔️ | ✔️
vertical | Boolean | false | 滑动方向是否为纵向	 | ✔️  | ✔️ | X | ✔️
previous-margin | String | "0px" | 前边距，可用于露出前一项的一小部分 | ✔️ | ✔️ | X | X
next-margin | String | "0px" | 后边距，可用于露出后一项的一小部分 | ✔️ | ✔️ | X | X
display-multiple-items | Number	 | 1 | 同时显示的滑块数量	 | ✔️ | ✔️ | X | ✔️ 
skip-hidden-item-layout | Boolean | false | 是否跳过未显示的滑块布局，设为 true 可优化复杂情况下的滑动性能，但会丢失隐藏状态滑块的布局信息 | ✔️ | Ｘ | X | X
bindchange | EventHandle |  | current 改变时会触发 change 事件，event.detail = {current: current, source: source} | ✔️ | ✔️ | X | ✔️
bindanimationfinish | EventHandle |  | 动画结束时会触发 animationfinish 事件，event.detail 同上 | ✔️ | ✔️ | X | X


注：需要使用ux.swiperTo控制滑块的移动，不可以直接对current进行操作


