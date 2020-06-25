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
  <br>font-weight属性用于设置文字的粗体大小。

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

