# 对css的学习

## 目录

### css的简介

### css的样式

### css选择器

### css属性

### css盒子模型

------

## 内容

### css的简介

**层叠样式表**（Cascading Style Sheets，缩写为 **CSS**）是一种[样式表](https://developer.mozilla.org/zh-CN/docs/Web/API/StyleSheet)语言，用来描述 [HTML](https://developer.mozilla.org/zh-CN/docs/Web/HTML) 或 [XML](https://developer.mozilla.org/zh-CN/docs/Web/XML/XML_introduction)（包括如 [SVG](https://developer.mozilla.org/zh-CN/docs/Web/SVG)、[MathML](https://developer.mozilla.org/zh-CN/docs/Web/MathML) 或 [XHTML](https://developer.mozilla.org/zh-CN/docs/Glossary/XHTML) 之类的 XML 分支语言）文档的呈现方式。CSS 描述了在屏幕、纸质、音频等其他媒体上的元素应该如何被渲染的问题。

简单而言就是在html的基础上进行加工，使之变精美且达到自己想要的个性化效果。



### css的样式

- 行内样式：在标签内部进行修改，但重复性高，并且不易维护与修改
- 内部样式：在<head>中进行说明，直观明了
- 外部样式：在另外一个css格式的新文件中进行说明，再在<head>中直接进行引用，可以在多文件中引用，但在学习初期时，查看比较麻烦

优先级：行内优先级>内部优先级=外部优先级

 		内部与外部谁优先遵从后来者居上原则



### css选择器

在进行对元素的修改时候，许多元素的标签是相同的，为了区别化地根据自己的需求进行修改，就需要用到选择器。css有许多选择器供我们使用。

- 通配选择器：*
- 元素选择器：h1,h2……
- 类选择器：.
- ID选择器：#
- 交集选择器：p.（类）……
- 并集选择器：p，.（类）……
- 后代选择器：space
- 子代选择器：>                   *子又有子，子又有孙，子子孙孙无穷匮也*
- 兄弟选择器：+和~两种，一种是向下相邻的下一个，一种是向下相邻的所有
- 属性选择器：以title举例：
  1. 选中具有title属性的元素:[title]
  2. 选中具有title属性且属性值为xxx的元素：[title="xxx"]
  3. 选中具有title属性且属性值以x开头的元素：[title^="x"]
  4. 选中具有title属性且属性值以x结尾的元素：[title$="x"]
  5. 选中具有title属性且属性值含x结尾的元素：[title*="x"]

### css的属性

1. 字体和文本属性：
   - font-family：设置字体族。
   - font-size：设置字体大小。
   - font-style：设置字体风格（如斜体）。
   - font-weight：设置字体粗细。
   - text-align：设置文本对齐方式。
   - text-decoration：设置文本装饰（如下划线）。
   - text-transform：设置文本大小写转换。
   - line-height：设置行高。
2. 颜色和背景属性：
   - color：设置文本颜色。
   - background-color：设置背景颜色。
   - background-image：设置背景图片。
   - background-repeat：设置背景图片是否重复。
   - background-position：设置背景图片的位置。
3. 盒子模型属性：
   - width：设置元素的宽度。
   - height：设置元素的高度。
   - padding：设置元素内部的空白区域。
   - margin：设置元素外部的空白区域。
   - border：设置元素的边框。
4. 定位属性：
   - position：设置元素的定位方式（如静态、相对、绝对、固定）。
   - top、right、bottom、left：设置元素相对于其正常位置的偏移。
   - z-index：设置元素的堆叠顺序。

### css盒子模型

CSS盒子模型是CSS中用于描述元素在页面上如何显示的一个概念模型。它包括元素的内容、内边距、边框和外边距四个部分。每个HTML元素在页面上都可以看作是一个矩形盒子，盒子模型定义了这个矩形盒子的各个组成部分。

理解CSS盒子模型对于布局和设计网页是非常重要的，因为它影响着元素在页面上的显示和定位。

1. **内容区域（Content Area）**：
   - 这是盒子模型的核心部分，也是元素实际内容所在的区域，比如文本、图片等。
   - 内容区域的尺寸由width和height属性控制。
2. **内边距（Padding）**：
   - 内边距是内容区域和边框之间的空间。
   - 内边距是透明的，不会影响元素的尺寸，但会影响元素的总宽度和高度。
   - 内边距可以通过padding-top、padding-right、padding-bottom、padding-left和padding属性来设置。
3. **边框（Border）**：
   - 边框围绕在内边距的外围，形成盒子的边界。
   - 边框可以有不同的样式（如实线、虚线等）、宽度和颜色。
   - 边框的宽度会加到元素的总宽度和高度上。
   - 边框可以通过border-top、border-right、border-bottom、border-left、border-width、border-style和border-color等属性来设置。
4. **外边距（Margin）**：
   - 外边距是边框外围的空间，用于在盒子之间创建距离。
   - 外边距是透明的，并且可以合并（collapsing margins）。
   - 外边距不会影响元素的总宽度和高度，但会影响元素在页面上的位置。
   - 外边距可以通过margin-top、margin-right、margin-bottom、margin-left和margin属性来设置。