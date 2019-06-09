## 盒模型

> W3C的标准盒模型
元素内容占据的空间是由width属性设置的，而内容周围的padding和border值是另外计算的；
即在标准模式下的盒模型，盒子实际内容（content）的width/height=我们设置的width/height;
盒子总宽度/高度=width/height+padding+border+margin

    .box {
        width: 200px;
        height: 200px;
        border: 20px solid black;
        padding: 50px;
        margin: 50px;
    }

>IE盒子模型(怪异盒模型)
在该模式下，浏览器的 width 属性不是内容的宽度，而是内容、内边距和边框的宽度的总和；
即在怪异模式下的盒模型，盒子的（content）宽度+内边距padding+边框border宽度=我们
设置的width(height也是如此)，盒子总宽度/高度=width/height + margin = 内容区宽度/高度 + padding + border + margin

    width(宽度),
    height(高度),
    margin:上 右 下 左;(外边距)
    margin-top:
    margin-right:
    margin-bottom:
    margin-left:
    padding:上 右 下 左;(内边距)
    padding-top:
    padding-right:
    padding-bottom:
    padding-left:
    border:1px solid red;(边框)
    border-width:;
    border-style:;
    border-color:;
    border-style:dotted(点状) solid(实线) double(双线) dashed(虚线);
    groove  定义 3D 凹槽边框。其效果取决于 border-color 的值。
    ridge   定义 3D 垄状边框。其效果取决于 border-color 的值。
    inset   定义 3D inset 边框。其效果取决于 border-color 的值。
    outset  定义 3D outset 边框。其效果取决于 border-color 的值。
    inherit 规定应该从父元素继承边框样式。

## 浮动

    基本属性
    1.float:left;元素向左浮动
    2.float:right;元素向右浮动
    3.float:none;默认值元素不浮动
    4.float:inherit;规定应该从父元素继承 float 属性的值

## 对齐方式

> html

    align 水平对齐
    align:left;左对齐
    align:right; 右对齐
    align:center; 居中对齐
    valign 垂直对齐
    valign:top; 上对齐
    valign:middle; 居中对齐
    valign:bototm; 底部对齐

> css

    text-align 水平对齐
    text-align:left;左对齐
    text-align:right; 右对齐
    text-align:center; 居中对齐
    vertical-align 垂直对齐
    vertical-align:top; 上对齐
    vertical-align:middle; 居中对齐
    vertical-align:bototm; 底部对齐

## 选择器

    1.全局通配符 *{}
    2.标签/元素选择器 p{} h1{}  table{} ul{}   b{} input{}
    3.类(class选择器可以被反复调用) .box{}  .left{}  .banzhang{}
    4.ID选择器具有唯一性 #box{} #left{} #banzhang{}
    5.包含选择器用 空格 隔开 #box h1{}
    6.群组选择器用 逗号 隔开 #box,#left{}
    7.伪类选择器
        .class:link{}    访问前的状态（正常状态）
        .class:visited{} 访问过后的状态
        .class:hover{}   鼠标滑过状态
        .class:active{}  鼠标点击状态、活动状态
    8.子类选择器 标识符 > 好处是缩小查找范围

## 优先级 （!important > 行内 > 内部 > 外部链接）

    行内 > ID > class / 类选择器 / 伪类 > 标签 / 元素
    先后优先级：后设的覆盖先设的
    远近优先级：行内 > id > class / 类选择器 > 标签 / 元素
    叠加优先级：越具体优先级越高
    指定大于继承  !important

## 文字 font

    font-color:   字体颜色
    font-size:    字体属性
    font-family:  字体格式(例：fony-family:"宋体";)
    font-weight:  字体加粗（值：bold加粗、normal正常字体/不加粗
    font-style:   字体样式（值：italic（倾斜）、normal正常字体）
    font-variant (字体变化): normal（正常）或small-caps（小体大写字母）
    简写顺序
    font:样式 , 变化 , 加粗 , 尺寸 , 行高 , 格式;

## 段落、文本

    line-height  行高（单位：px（像素） 百分比  em（包含自己，例子：空2格要写3em）
    text-align   文本水平对齐方式（值：left、center、right）
    text-indent  文本首行缩进，单位：px（像素）  em百分比 ）
    text-decoration  文本修饰（值：underline下划线、overline上划线、line-through删除线、none无）

## 背景：background（复合属性把多个background合并为一个）

    1.background-color--------背景颜色
      *.background-color:yellow; 英文单词代表的颜色名称
      *.background-color:#fff;   16进制用法，#f00 => #ff0000
      *.background-color:rgb(255,0,255); 用rgb代码表示
      *.background-color:transparent;    默认值，表示背景颜色为透明。

    2.background-image--------背景图（用url插图路径）

    3.background-position-----背景位置
      *.取值有3种:1.表示方向的关键词 2.百分比 3.position值像素或其他css单位
      1.表示方向的关键词
        *.位置：水平位置（上，中，下）、垂直位置（左，中，右）
        *.默认值：0% 0%
        *.如果只写了水平方向的关键词，那么垂直方向的关键词默认为center
      2.百分比
        *.依然是由两个值构成，即(水平方向的值 垂直方向的值)。
        *.0% 0%的取值代表左上角的位置，100% 100%的取值代表右下角的位置。
        *.如果只写了水平方向的取值，那么垂直方向的取值默认为50
      3.position值
        *.仍然是是由两个值构成，即(水平方向的值 垂直方向的值)
        *.0 0的取值代表左上角的位置
        *.一般都是使用像素（pixel）作为值的单位即px
        *.如果只写了水平方向的取值，那么垂直方向的取值默认为50%
      4.百分比的值（%）可以和position值混用。
        background-position: -144px 70%;
      5.必须先水平后垂直

    4.background-size--------背景图的尺寸
      *.length设置高度和宽度
        第一个为宽度,第二个为高度
        如果设置一个值，另一个值为auto
      *.percentage以百分比来设置背景图片宽度和高度
        第一个值设置宽，第二个值设置高
        如果设置一个值，另一个值为auto
      *.cover把背景图像扩展至足够大,以使背景图完全覆盖背景区域
      *.contian把图像扩展至最大尺寸,以使宽度和高度完全适应内容区域
      取值总共分为两大类：
       关键字取值（cover、contain）
        1.如果图片宽高不够，cover会将图片拉伸至足够大，直至铺满整个背景区域
        即使图片的其他部分无法显示在背景区域。（这样就相当于变相的放大图片至
        充满容器，才不管图片是否显示完整）
        2.而contain的做法是：自适应，即将图片扩展至最大尺寸，让图片的宽和高
        都刚好适应整个背景区域，不会存在显示部分图片的问题。（即使拉伸后，图
        片很不美观，也会完全铺满整个背景区域）
       非关键字取值（length、percentage）
        1.这两种取值都是用两个值来规定背景图片的尺寸，即第一个值代表宽度，第 二个值代表高度。
        2.而且，如果只设置其中的一个值，另外一个值会自动取值auto。
        3.其中，百分比取值是按照父元素的百分比来设置的

    5.background-repeat------背景重复
      *.repeat-------默认值
      *.repeat-y-----背景图在垂直方向重复
      *.repeat-x-----背景图在水平方向重复
      *.no-repeat----背景图将显示一次

    6.background-origin------背景图片定位区域
      *.padding-box----背景图相对于内边距来定位
      *.border-box-----背景图相对于边框来定位
      *.content-box----背景图相对于内容来定位

    7.background-clip--------背景绘制
      *.padding-box----背景被裁剪到内边距框
      *.border-box-----背景被裁剪到边框
      *.content-box----背景被裁剪到内容框

    8.background-attachment--规定背景图是否固定或者随着页面滚动
      *.scroll--------背景图会随着页面滚动而滚动
      *.fixed---------当页面其余部分滚动时背景图不会动

> 常用代码

    背景图自适应:
    .box{
        ackground-image:url(../image/Click_03_temp.png); background-repeat:no-repeat;
        background-size:100% 100%;
        -moz-background-size:100% 100%;
    }

    简写方式:顺序
    background: [background-color] 颜色
                [background-image] 背景图
                [background-repeat] 是否重复
                [background-attachment] 是否滚动
                [background-position] / [ background-size] 定位尺寸
                [background-origin]图片定位区域
                [background-clip];背景绘制
    .example {
        background: aquamarine
                    url(img.png)
                    no-repeat
                    scroll
                    center center / 50%
                    content-box content-box;
    }

### 未完续待 ...