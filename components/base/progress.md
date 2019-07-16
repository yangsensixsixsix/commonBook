#progress

进度条。


**属性及支持度**

属性|类型|默认值|说明|微信|百度|快应用|字节跳动|
---|---|---|---|---|---|---|
percent | Float | 无 | 百分比0~100 | ✔️ | ✔️ | ✔️ | ✔️
type | horizontal丨circular | horizontal | 进度条类型，不支持动态修改 | X | X | ✔️ | X
show-info | Boolean | false | 在进度条右侧显示百分比 | ✔️ | ✔️ | Ｘ | X
stroke-width | Number | 6 | 进度条线的宽度，单位px | ✔️ | ✔️ | Ｘ | ✔️
color | Color | #09BB07 | 进度条颜色 （请使用 activeColor） | ✔️ | ✔️ | Ｘ | ✔️
activeColor | Color |  | 已选择的进度条的颜色 | ✔️ | ✔️ | Ｘ | ✔️ 
backgroundColor | Color |  | 未选择的进度条的颜色 | ✔️ | ✔️ | Ｘ | ✔️
active | Boolean | false | 进度条从左往右的动画 | ✔️ | ✔️ | Ｘ | ✔️
active-mode | String | backwards | backwards: 动画从头播；forwards：动画从上次结束点接着播 |✔️  | ✔️ | Ｘ | ✔️
