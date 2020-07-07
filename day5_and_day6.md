# 第五天和第六天的学习笔记
  &nbsp;&nbsp;在css里，有两种类型的盒，块状盒（block boxes）和行内盒（inline boxes），这两者是通过display属性来区分的，可以
  设置display的属性为block或者inline来控制两种盒。与块状盒不同，行内盒并不会开启新的一行，而且并没有宽度和高度两个属性，在他身上
  水平的padding、margins或者borders都会被应用，使得其它行内元素与它间隔开。常见的块状盒标签包括:a和h1，常见的行内盒标签包括:
  a、span和strong等。其它可能用到的display属性值包括flex和grid。
  &nbsp;&nbsp;width和height勾画出盒模型主要内容的分布位置，padding和border描述了盒模型的内部边界，margin属性刻画的是盒
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
  next:对margin、padding及borders的介绍。
  
### 附加网址
&nbsp;&nbsp;[盒模型](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)
<br>

