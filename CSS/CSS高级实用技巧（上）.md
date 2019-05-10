双飞翼布局
html:xt

假等高效果，利用
padding：9999px；
margin:-9999px;
overflow：hidden；
----------------------------------------
css约定习惯
不要使用*，进行reset或者normalize
h5页面建议使用
html{box-sizing:border-box;}
 *，*：before，*：after{box-sizing:inherit;}
---------------------------------------------
字体图标
cssicon.space/

css hint
=================================================================
BFC
块级别的盒，参加块级别文档排列；
--------------------------------------
会生成BFC的元素：
    根元素
    float不为none的
    position为absolute 或者fixed
    display为 inline-block  table-cell  table-caption  flex inline-flex
    overflow不为visible

BFC的区域不与float box区域重叠
---------------------------------------------
清除浮动
overflow：hidden 会让内部元素参与容器元素高度的计算
----------------------------------------------
margin重叠的解决
同一个BFC内的两个block会margin重叠，让另一个block被BFC容器包裹
=================================================================
IFC 设置width height 没有效果

