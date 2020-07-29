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
    6. 建议启用IE Edge模式，建议在html标签上设置正确的lang属性。页面必须明确指定字符编码，指定字符编码的meta必须是head的
    第一个直接子元素，在编码时建议使用无BOM的utf-8编码。在引入css时，必须指名rel="stylesheet",在引入css和javascript时并无需
    指名type属性。展现定义放置在外部css中，行为定义放置在外部javascript中，结构-样式-行为的代码分离将有助于提高代码的可阅读性和
    可维护性。建议在head中引入所有需要的css资源，javascript最好放在页面的尾部。
    7. 页面必须有title标签声明标题，title必须作为head的直接子元素，位于charset之后。必须保证favicon.ico可访问，通常可以使用两种
    方法来实现，一种是在web server根目录下放置favicon.ico，另一种是使用Link来指定favicon。为保证页面对移动设备友好，建议指定页面
    的viewport。
    8. img标签的src取值不应该为空，避免为img添加不必要的title属性，应该为重要图片添加alt属性，应该添加width属性和height属性，
    有下载需求的图片应该采用img标签实现，无下载需求的图片采用css背景图实现。
    9. 有文本标题的控件必须使用label标签将其与其标题相关联。使用button元素时，必须指名type属性值，建议尽量不要使用按钮类元素的
    name属性。使用javascript进行表单提交时，应使原生提交功能正常工作。
    10. 要优先使用audio和video来定义音视频元素。
  * ### css编码规范
    1. 选择器与左括号之间必须有空格，属性名和冒号之间不能有空格，但是冒号和属性值之间必须有空格，列表属性值在书写时必须在逗号
    后买你紧跟空格。当使用多个选择器时，每个选择器必须单独占一行。'>'、'+'和'~'选择器的两遍需要保留一个空格。属性选择器
    中的值必须使用双引号包围。属性定义必须另起一行，以分号结尾。
    2. 无必要时，不能为id和class添加类型选择器进行限定。选择器的嵌套层级应不超过三级，位置靠后的限定条件应该精简。
    建议在可以使用属性缩写的情况下尽量使用属性缩写，使用属性缩写时也要考虑默认影响。在书写属性顺序时，建议以布局方式、
    盒模型、文本属性和视觉属性的顺序进行编写。当元素需要撑起高度，包含内部浮动元素时，尽量通过设置clear或者
    出发BFC的方式进行clearfix，尽量不使用增加空标签的方式。尽量不要使用!important声明。
    3. 文本内容必须用双引号包围，当数值为0-1的小数时可以省略0，url中的路径不加引号，rgb颜色必须使用
    #rrggbb，而不应该使用rgb()，颜色尽量使用缩写，但是不允许使用命名颜色值，必须同时给出水平和垂直的位置。
    4. font-family名字在一个项目中最好大小写统一，windows平台的字号应该不小于12px，font-weight必须使用数值
    方式进行描述。
    5. 使用transition时应该指定transition-property，尽量在浏览器能高效实现的属性上添加过渡和动画。media
    查询规则必须一起定义。带有私有属性前缀时应该由长到端排列，冒号位置对齐。禁止使用expression。
  * ### javascript编码规范
### 附加网址
&nbsp;&nbsp;[盒模型](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)
<br>&nbsp;&nbsp;[MDN-浮动](https://developer.mozilla.org/zh-CN/docs/<>Learn/CSS/CSS_layout/Floats)
<br>&nbsp;&nbsp;[学习css布局的网址](http://zh.learnlayout.com/)


