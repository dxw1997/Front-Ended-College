# 第五天和第六天的学习笔记
  &nbsp;&nbsp;在css里，有两种类型的盒，块状盒（block boxes）和行内盒（inline boxes），这两者是通过display属性来区分的，可以
  设置display的属性为block或者inline来控制两种盒。与块状盒不同，行内盒并不会开启新的一行，而且并没有宽度和高度两个属性，在他身上
  水平的padding、margins或者borders都会被应用，使得其它行内元素与它间隔开。常见的块状盒标签包括:a和h1，常见的行内盒标签包括:
  a、span和strong等。其它可能用到的display属性值包括flex和grid。
  <br>&nbsp;&nbsp;width和height勾画出盒模型主要内容的分布位置，padding和border描述了盒模型的内部边界，margin属性刻画的是盒
  的外部边界，它也影响盒模型在页面上的展示。在一种实现（实现A）中，border和padding被计算在了宽和高之内，在另一种实现中，并没有被计算在内。
  可以设置box-sizing:border-box来将盒模型设置为实现A,下面的这段代码片段可以将这整个文档的默认设置改为实现A。  
  ```
   html{
    box-sizing: border-box;
   }
   *, *::before, *::after {
    box-sizing: inherit;
   }
  ```
  <br>&nbsp;&nbsp;margin属性会在盒模型周围设置一块看不到的空间，如果将它设置为一个负数，那么这块区域将可以和其它区域重叠。
  如果两个个margin的边界重合，而且数值并不相同，那么他们将会发生边界塌陷。
  <br>&nbsp;&nbsp;在使用padding时，你不能将它的数值设置为负数。
  <br>&nbsp;&nbsp;在inline和block之间有一种折中--inline-block，它不会创建新的行，而且会保存宽度和高度
  这两个属性。
  <br>&nbsp;&nbsp;浮动最初是用来再文本内浮动图像的。clear属性可以前面元素浮动对于当前元素的影响。取值可以为'left'、'right'
  和'both'。有时，浮动会使得内部元素"溢出"，为了改变这种状况，可以将它的父元素的overflow属性设置为auto。
  <br>
  <br>&nbsp;&nbsp;为什么需要有编码规范呢？杂乱的编码既不容易理解，也不容易在将来进行维护，而编码规范则有助于解决这两个
  问题。
  * ### html编码规范<br>
    1. 使用四个空格为一个缩进层级，script或者style标签的缩进与script或者style标签的缩进同等级别，建议每行
    字符不超过120个。
    2. class的命名必须全字母小写，使用-进行单词分割，代表相应模块或部件的内容或功能，而不应该使用样式信息
    元素id同样必须保证页面唯一，同时，id和class应该尽量地短。
    3. class应该具有明确的语义和样式，否则容易导致css泛滥，在javascript中使用id和属性选择是更好的方式。
    在同一个页面上，应该避免使用相同的name和id。
    4. 标签名必须使用小写字母；无需自闭合的标签，不允许自闭合，可选闭合的标签，必须使用闭合标签，在代码体积要求严格的地方
    可以例外；标签使用必须符合标签嵌套规则，同时每个标签的使用必须符合相应语义。尽量减少标签的使用，尽量使用css完成表格布局
    的效果。
    5. 属性名必须使用小写字母，属性值则必须使用双引号包围。布尔类型的属性，建议不添加属性值，自定义属性建议以xxx-为前缀，推荐
    使用‘data-’。
  * ### css编码规范
  * ### javascript编码规范
### 附加网址
&nbsp;&nbsp;[盒模型](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)
<br>&nbsp;&nbsp;[MDN-浮动](https://developer.mozilla.org/zh-CN/docs/<>Learn/CSS/CSS_layout/Floats)
<br>&nbsp;&nbsp;[学习css布局的网址](http://zh.learnlayout.com/)


