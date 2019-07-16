# position-view
基本容器，需要添加属性position:relative,且直接子组件需全部添加属性position:absolute，此时每个直接子组件按照先后顺序依次堆叠，覆盖前一个子组件。

示例：
```
<template>
    <position-view class="box">
        <view class="contentOne">1</view>
        <view class="contentTwo">2</view>
        <view class="contentThree"><3/view>
    </position-view>
</template>

<style>
.box{
    position:relative;
}
.contentOne{
    position:absolute;
}
.contentTwo{
    position:absolute;
}
.contentThree{
    position:absolute;
}
</style>
```