# 第三天学习笔记
  为了在github上用md文件来记录自己的学习笔记，首先应该学习github上的相关markdown语法，readme文件也主要是用markdown语法来进行书写的。可用于readme编写的两个参考网址，[csdn上的blog](https://blog.csdn.net/wsymcxy/article/details/82749527),[另外一个github地址](https://github.com/guodongxiaren/README#%E4%BA%8C%E7%BA%A7%E6%A0%87%E9%A2%98)。

## 基本文本和字体样式
  用于css的样式文本通常分为两类:字体样式和文本布局风格。字体样式会直接作用到字体上，文本布局通常用于调整布局。
  可以使用的字体样式属性有color,font-family,font-size, font-weight, text-transform, text-decoration,
  text-shadow;文本的布局属性包括text-align, line-height, letter-spacing, word-sapcing;上面的这些属性都是经常使用的
  一些属性，下面进行比较详细的介绍。
  
  color属性可以设置一些字体的颜色值，具体数值是合法的css颜色单位。<br>
  font-family属性会为文本设置一个不同的字体，如果设置的字体不可用，那么将会使用默认字体代替，可使用的字体类型'serif'、'sans-serif'、'monospace'、'cursive'、'fantasy'，如果要查找可用字体,可以去网址[cssfontstack.com](https://www.cssfontstack.com/)去查找。
也可以使用字体栈的方式来增强代码的健壮性。
  <br>font-size属性可以用于设置字体大小，虽然有px、em和rem三种单位，但是我觉得直接使用px单位就可以了，复杂情况在去查找文档和资料等。
em和rem比较的分别是从父单位及根单位开始。
  <br>font-style属性用来设置文本的斜体表示，normal值、italic值及oblique值分别表示将字体设置为普通字体、斜体及倾斜字体的模拟。
  <br>font-weight属性用于设置文字的粗体大小，可以设置为普通-normal、加粗-bold、lighter或者bolder，也可以使用一些数值粗体值。
  <br>text-transform设置要转换的字体，属性值包括none、uppercase、lowercase、capitalize（让所有单词首字母大写）和full-width(让所有
  字形转成全角)
  <br>text-decoration属性用于设置文本的线装饰，包括没有(none)、下划线(underline)、上划线(overline)和穿过文本（line-through）。
  <br>text-shadow属性用于为文本应用设置阴影，需要设置的四个值分别是水平位移、垂直位移、模糊半径和阴影的基础颜色；也可以来设置多种阴影。
  <br>text-align属性用于控制文本如何对齐，可以设置为left、right、center和justify。justify会使文本展开，改变单词之间的差距。
  <br>line-height属性用于设置每行文本之间的高，通常是字体大小的一定倍数值。
  <br>letter-spacing或者word-spacing属性用于设置字母和字母之间或者是单词和单词之间的间距。

  在熟悉上面的这些属性之后，可以探索的一些属性，现在用不到，将来可能会用到
  <br> <b>字体样式:</b>
  - font-variant:在小型大写字母和普通文本选项之间切换。
  - font-kerning:开启或关闭字体间距选项
  - font-feature-settings:开启或关闭不同的OpenType字体特性
  - font-variant-alternates:控制给定的自定义字体的替代字形的使用
  - font-variant-caps:控制大写字母替代字形的使用
  - font-variant-east-asian:控制东亚文字替代字形的使用，比如日语和汉语
  - font-variant-ligatures:控制文本中使用的连写和上下文形式
  - font-variant-numeric:控制数字、分式和序标的替代字形使用
  - font-variant-position:控制位于上标或下标处，字号更小的替代字形的使用
  - font-variant-adjust:独立于字体的实际大小尺寸，调整其可视大小尺寸
  - font-stretch:在给定字体的可选拉伸版本中切换
  - text-underline-position:指定下划线的排版位置
  - text-rendering: 尝试执行一些文本渲染优化
  <br> <b>文本布局样式:</b>
  - text-indent:在文本内容的第一行前应该留出多少的水平空间。
  - text-overflow:定义如何向用户表示存在被隐藏的溢出内容
  - white-space:定义如何处理元素内部的空白和换行
  - word-break: 指定能否在单词内部换行
  - direction:定义文本的方向
  - hyphens: 为支持的语言开启或关闭连字符
  - line-break: 对东亚语言采取更强或更弱的换行规则
  - text-align-last: 定义一个块或行的最后一行，恰好位与一个强制换行前，如何对齐
  - text-orientation:定义行内文本的方向
  - word-wrap: 指定浏览器是否可以在单词内换行以避免超出范围
  - writing-mode:定义文本行布局为水平还是垂直，以及后继文本流的方向

## css的几个问题
  css（cascading style sheets）用来对网页进行风格设计和布局设置。
  <br>浏览器是怎么将css和html变为网页的呢？当然在这个转换过程中，也使用了javascript，但是
  为了简单，这里不考虑js。浏览器从网络中接收到html文档之后，将它转换成为了DOM，DOM被存储
  在内存之中，之后浏览器将html的关联资源都取来，包括css等，之后浏览器进行css解析等，之后浏览器
  就进行了渲染及显示。
  <br>DOM具体说来是将文档内容解析之后的树结构，[这是DOM对象的一个讲解示例](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/How_CSS_works)
  可以看里面的about the DOM这部分。
  <br>如果浏览器在解析css文件时碰到了它读不懂的东西，它会将这些东西忽略掉。可以将一些较新的css
  属性值等用于网页展现的提升。
  <br>在使用css时，可以使用外部链接，比如<link rel="stylesheet" href="xxx.css">这里css文件换成
  对应的css文件路径地址就可以了。也可以直接在<head>内部的<style>标签中直接书写css的内容。也可以
  在标签中直接设置style属性来直接设置css样式。
  <br>如果两个css选择器的内容一致，可以用逗号将他们隔开，后面书写相同的内容。当选择器错误时，所有
  选择器内部的内容都会被忽略。选择器的三种类型包括标签、类和ID。除此之外,还有属性或者动作的选择器，
  包括带有结构的选择器。
  <br>
  
## 附加的网址资源
  [html5手册](http://caibaojian.com/html5/default.htm)
  <br>[MDN-CSS介绍]()
  <br>[MDN-CSS如何工作]()
  <br>[MDN-CSS语法]()
  <br>[MDN-选择器](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors)
  <br>[MDN-简单选择器]()
  <br>[MDN-属性选择器]()
  
  
  
  
