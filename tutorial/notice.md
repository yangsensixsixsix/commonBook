##注意

###CSS书写规范
1、使用flex+px布局。

2、box-shadow在快应用中不起作用。

3、不要用space-around,需要用space-between代替。

4、字重font-weight不要用数字精确值，要用normal或bold两种。

5、颜色必须使用16进制，可以缩写（#df0,#ddff00）。

6、最外层元素不要用for循环，需要在最外面再包一层。(快应用不支持最外层元素循环渲染);

7、背景颜色要设置成background-color。

###HTML书写规范

    标签上不可以写style样式。position:absolute属性下的left,right,top,bottom属性除外。

###JS书写规范

    全局变量和外部引入必须写在Component上方。