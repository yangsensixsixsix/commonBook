#image
图片。


**属性及支持度**

属性|类型|默认值|说明|微信|百度|快应用|字节跳动
---|---|---|---|---|---|---|
src | String |  | 图片资源地址 | ✔️ | ✔️ | ✔️ | ✔️ 
alt | String |  |加载时显示的占位图；只支持本地图片资源 | Ｘ| Ｘ | ✔️ | X
mode | String | 'scaleToFill' | 图片裁剪、缩放的模式 | ✔️ | ✔️ | Ｘ | ✔️ 
lazy-load | Boolean | false | 图片懒加载。只针对 scroll-view 下的 image 有效 | ✔️ | ✔️ | Ｘ | ✔️ 
binderror | HandleEvent |  | 当错误发生时，发布到 AppService 的事件名，事件对象 event.detail = {errMsg: ‘something wrong’} | ✔️ | ✔️ | Ｘ | ✔️ 
bindload | HandleEvent |  | 当图片载入完毕时，发布到 AppService 的事件名，事件对象 event.detail = {height:’图片高度px’, width:’图片宽度px’} | ✔️ | ✔️ | Ｘ | ✔️ 


mode有效值：

模式 | 值 | 说明
---|---|--- 
缩放 | scaleToFill | 不保持纵横比缩放图片，使图片的宽高完全拉伸至填满 image 元素
缩放 | aspectFit | 保持纵横比缩放图片，使图片的长边能完全显示出来。也就是说，可以完整地将图片显示出来
缩放 | aspectFill | 保持纵横比缩放图片，只保证图片的短边能完全显示出来。也就是说，图片通常只在水平或垂直方向是完整的，另一个方向将会发生截取
缩放 | widthFix | 宽度不变，高度自动变化，保持原图宽高比不变
裁剪 | top | 不缩放图片，只显示图片的顶部区域
裁剪 | bottom | 不缩放图片，只显示图片的底部区域
裁剪 | center | 不缩放图片，只显示图片的中间区域
裁剪 | left | 不缩放图片，只显示图片的左边区域
裁剪 | right | 不缩放图片，只显示图片的右边区域
裁剪 | top left | 不缩放图片，只显示图片的左上边区域
裁剪 | top right | 不缩放图片，只显示图片的右上边区域
裁剪 | bottom left | 不缩放图片，只显示图片的左下边区域
裁剪 | bottom right | 不缩放图片，只显示图片的右下边区域