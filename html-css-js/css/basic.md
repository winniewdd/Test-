内嵌式：css写在style里面
外联式：单独的css
行内式：写在标签里面

### 基础选择器
标签选择器：P{}
类选择器：.class{} / class="class"多个选择器选择用空格隔开。名字：数字，字母，下划线，中划线，不能以数字开头
id选择器：#id{} / id="id"，id名唯一，不可重复使用。

### 文本操作
font-size:60px
font-weight:400/700
font-style:intalic/normal 倾斜
font-family:宋体,sans-serif
font-indent:2em 首行缩进
font-docration:underline
<!-- underline:下划线 line-through：删除线 overline：上划线 none：去掉下划线 -->
text-align:center/left/right
line-height:30px,行高
font: style 

### 进阶选择器
1.后代选择器：
父代空格后代引号
div p{  
}
2.子代选择器：
父代>子代{
}
div>p{
}
3.并集选择器
a,p,div,span{}
4交集选择器
标签.class
p.box{}
5.hover伪类选择器
a:hover

### 背景
1.背景颜色 background-color:red #111111 rgba(0,0,0,0,0.5)
2.背景图片 background-image:url()
3.背景平铺 background-repeat:norepeat
4.背景位置 background-position:right 0；center bottom；center center；(10px 100px)
backgroud:color image repeat position

### 元素显示模式
1.块级模式：div，竖排列，大小可更改
2.行内模式：span，横排列，大小不可更改
3.行内快模式：input，button，行排列大小可更改
4.元素显示模式转换
display:block，块级元素
display:inline-block，行内快
display:inline，行内

继承性：
控制文字属性（color，font）可以继承，其他属性不可以。
特殊：a标签color失效，h标签font-size失效

层叠性：
下面样式覆盖上面的
不同选择器样式同时生效

选择优先级：
继承 <通配符* < 标签选择器< 类选择器 < id选择器 < 行内样式 < !important
div{
    color:green !important
}

权重叠加计算：
第1-4级：行内，id，类，标签
一级一级比较数量
若数量相同比较层叠性
！important最高

### 盒子
内容 content ，内边距 padding，边框 border，外边距 margin，
内容：width height background-color
边框：border，复合属性。
    border：10px solid red  大小，线，颜色，空格隔开不分先后。
    线：dashed虚线 solid实线，dotted点线
    单方向线：属性名更改border-left/right/bottom/top
盒子大小=width+border，height+border

内边距：
padding:10px
复合属性：padding: 10px 10px 10px 10px 上左下右
内减模式：box-sizing: horder-box

外边距：
margin:上左下右

清除默认内外边距：
*{
    margin:0;
    padding:0;
}

版心居中：
    margin: 0 auto；

伪元素：
使用css创建内容

.class::before{
    content:'mouse';
}
.class::after{
    content:'mi';
}
<div class="class">love</div>

页面显示老鼠爱大米


### 标准流

div span等标准的排列形式

浮动：
作用：完美的网页布局，使块元素在一行排
块元素：使用display：line-block，会在同一行，但有空格，解决方法：把两个div标签在同一行写
案例：
.one{
    float:left
}
.two{
    float:left
}
结果：两个dev在同一行且中间无空格

浮动特点：
1.不占用标准流的位置，半脱离

书写css：
1.浮动 / display
2.盒子模型： margin border padding 宽高背景色
3.文字样式

导航条：nav，用li嵌套a
