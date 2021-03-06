# 第四天教程的学习笔记

  &nbsp;&nbsp;&nbsp;首先需要进行阅读的材料:[w3school的css背景](https://www.w3school.com.cn/css/css_background.asp)、[MDN的背景和边界](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Backgrounds_and_borders)
  background-color属性可以用来为元素设置背景色，值可以为任何合法的颜色值，其默认值为transparent，这样
  可以显示它父元素的颜色。
  <br>&nbsp;&nbsp;&nbsp;background-image属性可以将图片设置为背景，使用时的格式是url(xx路径)。如果想对图像进行铺展，可以设置属性
  background-repeat的值为repeat-x或者repeat-y。
  <br>&nbsp;&nbsp;&nbsp;background-position可以设置图像的放置位置，用关键字top、bottom、
  left、right和center来成对的设置，如果只是用了一个关键字，那么另一个关键字默认为center；它的值也同样可以使用成对
  的百分比来表示，比如'66% 33%'，这表示将一个背景图像放置在水平方向2/3，垂直方向1/3处；最后，同样可以使用成对的像素值
  来设置背景的位置。
  <br>&nbsp;&nbsp;&nbsp;background-attachment属性的默认值为scroll，意思是在默认的情况下，背景图像会随文档滚动，同样可以设置它的值为fixed来固定背景图像相对于可视区域的位置。
 <br>&nbsp;&nbsp;&nbsp;在插入背景图片后，可以使用background-size属性来控制要显示的图片大小，比如长和宽两个属性设置为像素值，也可以使用
 'contain'和'cover'两个值，这两个值都保留了长宽比，但是一个会将图像完全包括在内，一个会填满整个区域。
 <br>&nbsp;&nbsp;&nbsp;可以在background-image属性的后面设置gradient来控制颜色的渐变,附加网址的菜鸟教程讲的比较详细。
 <br>&nbsp;&nbsp;&nbsp;在使用多个背景图片时也类似于使用单个背景图片，只不过他们之间需要使用逗号分隔开，其他相关控制背景图片的属性在使用时也用多个逗号隔开即可。
 <br>&nbsp;&nbsp;&nbsp;border用于设置边界的属性，主要有width、style和color三个子属性，可以设置相应边界的具体形式。style的值可以设置为dashed、solid、dotted、double和none，意思分别是虚线、点线、实线、双线和没有边界。如果需要对每个边界进行一次设置，需要用top-right-
 bottom-left的顺序。如果边界风格设置为none,那么再去设置边界的其他属性是没有意义的。border-radius属性可以设置边界的几个角的
 半径。
 <br>&nbsp;&nbsp;&nbsp;list-style-type可以改变列表项的标志类型，它可以使用的值较多，可以看附加网址中的对应网址。list-style-image会对
 各个标志使用相应的图像。ul中type常用的值为'disc'、'circle'、'square'和'none'。ol中的type更多是对数字等的修饰，比如
 'decimal'、'lower-roman'、'upper-roman'、'lower-alpha'和'upper-alpha'等。list-style-position属性会涉及每个列表项的
 放置位置，'inside'会将列表项缩进，'outside'会使得列表项不缩进。同样可以在li标签中使用background-image的相关属性。ol
 标签的start属性可以使得列表项从其他值开始计数， revised属性将会使得ol的表项进行倒计数。value属性可以直接作用到li标签上
 设置相应li标签的实际显示值。
 <br>&nbsp;&nbsp;&nbsp;链接标签-a标签，有着四种状态：link、visited、hover和active，在设置标签状态时，hover必须位与link和visited之后，active状态必须位与hover之后。链接的支持设置属性有color、font-family、background等等。
 <br>&nbsp;&nbsp;&nbsp;在css中，子元素一般是从父元素继承属性，但也有不继承属性的情况。如果要避免父元素对子元素的影响，直接进行更加详细的书写就行。
 <br>&nbsp;&nbsp;&nbsp;派生选择器:依据元素在其位置的上下文关系来定义样式，从而使得标记更加简洁。比如li strong， 这将会选择li标签下的strong标签。
 <br>&nbsp;&nbsp;&nbsp;':first-child'伪类选择器总会选择第一个子元素。可以进一步学习的几个子选择器：'last-child'、'only-child'、
 'invalid'。
 <br>&nbsp;&nbsp;&nbsp;'::first-line'伪元素选择器。'::before'和'::after'会额外插入一些元素。[这个网址](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Pseudo-classes_and_pseudo-elements)的最下面有一些可以参考的选择器样式。
 <br>&nbsp;&nbsp;&nbsp;降序选择器，如果子元素的标签结构像所写的这样，就会被选中。
 <br>&nbsp;&nbsp;&nbsp;孩子选择器，'>'会直接选择孩子标签进行设置。
 <br>&nbsp;&nbsp;&nbsp;邻接选择器，'+'会选择直接邻接的两个标签的后一个。
 <br>&nbsp;&nbsp;&nbsp;通用邻接选择器，'~'在选择子标签时并不要求必须相邻。
 <br>&nbsp;&nbsp;&nbsp;specificity是浏览器在应用css规则时所依据的先后次序，标签选择器优先级更低，类选择器优先级更高。在css选择器具有相同的specificity时，最后一个css选择器会实际发挥效果，这点称为css选择器的顺序性。有一些父标签的css属性会被子标签继承，有些不会。像宽度、外边距、
 内边距和边界这些属性都不会继承。
 <br>&nbsp;&nbsp;&nbsp;控制属性继承的几个值，'inherit'、'initial'和'unset'分别意味着使用父标签的属性值，使用该
 默认的属性值和如果由继承来的属性值就使用继承过来的属性值，否则使用初始属性值。
 <br>&nbsp;&nbsp;&nbsp;设置all属性为'unset'可以恢复所有属性的默认值。
 <br>浏览器依据三条规则决定怎么应用css选择器:importance、specificity和source order。source order意味着，如果浏览器解析到了具有相同重要程度的代码，那么它将会选择保留位置较为靠后的那个css代码。在specificity中，直接设置style属性的重要性最高，其次是使用ID选择器，其次是使用类选择器、属性选择器和伪类选择器，其次是使用标签选择器。但具体重要性程度的计算仍然比较复杂，具体看是使用了几个几种级别的标签，把相应级别重要性的数值加到最终值上即可。伪元素选择器的重要性是最低的----1。几个较低重要性的标签组合之后，可能会超过特别重要的标签。
 <br>'!important'放在属性值的后面可以增强该属性，使它持续发挥作用；除非后面有其它'!important'来改写其它属性值。

## 附加网址
  [可以玩一下的css gradient网址](https://cssgradient.io/)
  <br>[菜鸟教程对css渐变的讲解](https://www.runoob.com/css3/css3-gradients.html)
  <br>[设置list-style-type时可以使用的属性值](https://www.w3school.com.cn/cssref/pr_list-style-type.asp)
  <br>[w3school的css背景](https://www.w3school.com.cn/css/css_background.asp)
  <br>[MDN的背景和边界](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Backgrounds_and_borders)
  <br>[MDN的样式列表](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/%E4%B8%BA%E6%96%87%E6%9C%AC%E6%B7%BB%E5%8A%A0%E6%A0%B7%E5%BC%8F/Styling_lists)
  <br>[css选择器的英文介绍](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Pseudo-classes_and_pseudo-elements)
  <br>[选择器的组合](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Combinators)
  <br>[编码器的优先级](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance)


