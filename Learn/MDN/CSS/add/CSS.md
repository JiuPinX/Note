# 入门

## [CSS 语法](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/First_steps/What_is_CSS#css_语法 "Permalink to CSS 语法")

CSS 是一门基于规则的语言 —— 你能定义用于你的网页中特定元素样式的一组规则。比如“我希望页面中的主标题是红色的大字”

下面这段代码使用非常简单的 CSS 规则实现了之前提到的效果：

```
h1 {
    color: red;
    font-size: 5em;
}
```

语法由一个 [选择器 (selector)](https://developer.mozilla.org/zh-CN/docs/Glossary/CSS_Selector)起头。它 _选择 (selects)_ 了我们将要用来添加样式的 HTML 元素。在这个例子中我们为一级标题（主标题[`<h1>` (en-US)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements "Currently only available in English (US)")）添加样式。

接着输入一对大括号`{ }`。在大括号内部定义一个或多个形式为 **属性 (property):值 (value);** 的 **声明 (declarations)**。每个声明都指定了我们所选择元素的一个属性，之后跟一个我们想赋给这个属性的值。

冒号之前是属性，冒号之后是值。不同的 CSS [属性 (properties) (en-US)](https://developer.mozilla.org/en-US/docs/Glossary/property/CSS "Currently only available in English (US)") 对应不同的合法值。在这个例子中，我们指定了 `color` 属性，它可以接受许多[颜色值](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Values_and_units#%E9%A2%9C%E8%89%B2)；还有 `font-size` 属性，它可以接收许多 [size units](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Values_and_units#%E6%95%B0%E5%AD%97%EF%BC%8C%E9%95%BF%E5%BA%A6%E5%92%8C%E7%99%BE%E5%88%86%E6%AF%94) 值。

一个 CSS 样式表可以包含很多个规则。

```
h1 {
    color: red;
    font-size: 5em;
}

p {
    color: black;
}
```

你会发现你已经很快掌握了一些属性的值，但是属性可以接受的值远不止这些。在 MDN 上每个属性都有单独的页面，不论你是忘记了某个属性，还是想要知道一个属性还能接受什么其它的值，这些页面都可以帮助你。

**备注：** 在 MDN 上的 [CSS reference](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference) 页面列举了所有的 CSS 属性页面（同时也包括其它的 CSS 特性）。另外，当你想要寻找一个 CSS 特性的更多内容时，多使用你的搜索引擎来搜索 "mdn _css-feature-name_" 。例如，搜索 "mdn color" 和 "mdn font-size"！

## [CSS 模块](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/First_steps/What_is_CSS#css_模块 "Permalink to CSS 模块")

你可以通过 CSS 为许多东西添加样式，CSS 由许多_模块 (modules)_ 构成。你可以在 MDN 上浏览这些模块的参考内容 (MDN reference)，许多模块都被组织在自己单独的文档页面。例如，我想查找一下 MDN reference 的 [Backgrounds and Borders](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_Backgrounds_and_Borders) 模块的相关内容，来了解它是用来做什么的、它还包括什么属性、它还有什么其它特性等。你也可以在 _CSS Specification_ 查找（见下文），它定义了 CSS 规范。

在这个阶段你不必过于担心 CSS 是如何组织的 (how CSS is structured)，但是它能帮助你更好的掌握 CSS。例如，你注意到某个属性和另外一些属性的相似点，并且它们可能确实是相同的格式。

举个具体点的例子：如上文中的 Backgrounds and Borders 模块 — 你会发现 [`background-color`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/background-color) 和 [`border-color`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/border-color) 这两个属性在逻辑上相通。并且它也确实如此。

## [添加 CSS 试试看？](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/First_steps/Getting_started#添加_css_试试看？ "Permalink to 添加 CSS 试试看？")

我们最想做的就是让 HTML 文档能够遵守我们给它的 CSS 规则。其实有三种方式可以实现，而目前我们更倾向于利用最普遍且有用的方式——在文档的开头链接 CSS。

在与之前所说的 HTML 文档的相同目录创建一个文件，保存并命名为 `styles.css` 。（看后缀知道此文件就是 CSS 文件）

为了把 `styles.css` 和 `index.html` 连接起来，可以在 HTML 文档中，[`<head>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/head) 语句模块里面加上下面的代码：

```
<link rel="stylesheet" href="styles.css">
```

[`<link>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/link) 语句块里面，我们用属性 `rel`，让浏览器知道有 CSS 文档存在（所以需要遵守 CSS 样式的规定），并利用属性 `href` 指定，寻找 CSS 文件的位置。你可以做测试来验证 CSS 是否有效：在 `styles.css` 里面加上 CSS 样式并观察显示的结果。下面，用你的编辑器打出下面的代码。

```
h1 {
  color: red;
}
```

保存 HTML 和 CSS 文档，刷新浏览器网页，不出意外你将看到网页顶层的大标题变成红色了。如果看到这个现象，恭喜你：你已经成功将某些 CSS 样式运用到 HTML 上了。当然假设没有达到预想结果，可以仔细检查每句代码是否正确，加油：）

你可以一直在本地编辑器练习 `styles.css` ，或者采用我们教程下面的交互式智能编辑器。这个编辑器会默认把第一个面板里面的 CSS 代码连接到旁边的 HTML 文档，就好像我们上面得两个文档一样互相连接。

## [改变元素的默认行为](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/First_steps/Getting_started#改变元素的默认行为 "Permalink to 改变元素的默认行为")

只要一个 HTML 文档标记正确，即使像我们的例子那么简单，浏览器都会尽全力将其渲染至可读状态。标题默认使用大号粗体；列表旁总有项目符号。这是因为浏览器自带一个包含默认样式的样式表，默认对任何页面有效。没有了它们，所有文本会夹杂在一起变得一团糟，我们只得从头开始规定，好糟糕。话说回来，所有现代浏览器的默认样式都没什么差距。

不过你可能对浏览器的默认样式不太满意。没关系，只需选定那个元素，加一条 CSS 规则即可。就拿我们的无序列表 `<ul>`举个例子吧，它自带项目符号，不过要是你跟它有仇，你就可以这样移除它们：

```
li {
  list-style-type: none;
}
```

把上述代码加到你的 CSS 里面试一试！

欢迎参阅 MDN 上的 `list-style-type` 属性，看看到底有哪些值被支持。 [`list-style-type`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/list-style-type) 页首提供互动性示例，您可以输入不同的值来瞅一瞅它们到底有什么用。关于每个值的详细描述都规规整整地列在下面。

通过参阅上述页面，你会发现你不仅能移除项目符号——你甚至能改变它们。赶快试试 `square`，它能把默认的小黑球变成方框框。

## [样式化 HTML 元素](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/First_steps/Getting_started#样式化_html_元素 "Permalink to 样式化 HTML 元素")

通过上一节将大标题变成红色的例子，我们已经展示了我们可以选中并且样式化 HTML 元素。我们通过触发元素选择器实现这一点——元素选择器，即直接匹配 HTML 元素的选择器。例如，若要样式化一个文档中所有的段落，只需使用选择器 `p`。若要将所有段落变成绿色，你可以利用如下方式：

```
p {
  color: green;
}
```

用逗号将不同选择器隔开，即可一次使用多个选择器。譬如，若要将所有段落与列表变成绿色，只需：

```
p, li {
    color: green;
}
```

## [使用类名](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/First_steps/Getting_started#使用类名 "Permalink to 使用类名")

目前为止，我们通过 HTML 元素名规定样式。如果你愿意所有元素都一个样，也不是不可以，但大多数情况下，我估计你都不愿意。我知道你想干啥，你想用这种方式样式化这一片元素，又想用那种方式样式化那一片元素，真贪心。不过没关系，你可以给 HTML 元素加个类名（class），再选中那个类名，这样就可以了，大家基本上都这么用。

举个例子吧，咱们把 [class 属性](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Global_attributes/class)加到表里面第二个对象。你的列表看起来应该是这样的：

```
<ul>
  <li>项目一</li>
  <li class="special">项目二</li>
  <li>项目 <em>三</em></li>
</ul>
```

在 CSS 中，要选中这个 `special` 类，只需在选择器的开头加个西文句点（.）。在你的 CSS 文档里加上如下代码：

```
.special {
  color: orange;
  font-weight: bold;
}
```

保存再刷新，就可以看到变化。

这个 `special` 类型可不局限于列表，它可以应用到各种元素上。举个例子，你可能也想让段落里边的 `<span>` 一起又橙又粗起来。试试把`special` 类属性加上去，保存，刷新，哇，生活就是这么美好。

有时你会发现选择器中，HTML 元素选择器跟类一起出现：

```
li.special {
  color: orange;
  font-weight: bold; 
}
```

这个意思是说，“选中每个 `special` 类的 `li` 元素”。你真要这样，好了，它对 `<span>` 还有其它元素不起作用了。你可以把这个元素再添上去就是了：

```
li.special,
span.special {
  color: orange;
  font-weight: bold;
}
```

你们都是懒人，肯定不想每加一个 special 类的元素就改一遍 CSS 表，你肯定想把一个类的属性应用到多个元素上。所以说，有时还是别管元素，光看类就完事了，除非你意志坚定，坚持对这个类的某一种元素创造规则，还不让其它元素用。

## [根据元素在文档中的位置确定样式](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/First_steps/Getting_started#根据元素在文档中的位置确定样式 "Permalink to 根据元素在文档中的位置确定样式")

有时候，您希望某些内容根据它在文档中的位置而有所不同。这里有很多选择器可以为您提供帮助，但现在我们只介绍几个选择器。在我们的文档中有两个 `<em>`元素 ——一个在段落内，另一个在列表项内。仅选择嵌套在`<li>` 元素内的`<em>`我们可以使用一个称为**包含选择符**的选择器，它只是单纯地在两个选择器之间加上一个空格。

将以下规则添加到样式表。

```
li em {
  color: rebeccapurple;
}
```

该选择器将选择`<li>`内部的任何`<em>`元素（`<li>`的后代）。因此在示例文档中，您应该发现第三个列表项内的`<em>`现在是紫色，但是在段落内的那个没发生变化。

另一些可能想尝试的事情是在 HTML 文档中设置直接出现在标题后面并且与标题具有相同层级的段落样式，为此需在两个选择器之间添加一个 `+` 号 (成为 **相邻选择符**)

也将这个规则添加到样式表中：

```
h1 + p {
  font-size: 200%;
}
```

位于 `h1` 后面的 `p` 字体大小直接上 200% 了。

## [根据状态确定样式](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/First_steps/Getting_started#根据状态确定样式 "Permalink to 根据状态确定样式")

在这篇教程中我们最后要看的一种修改样式的方法就是根据标签的状态确定样式。一个直观的例子就是当我们修改链接的样式时。当我们修改一个链接的样式时我们需要定位（针对） [`<a>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/a) （锚）标签。取决于是否是未访问的、访问过的、被鼠标悬停的、被键盘定位的，亦或是正在被点击当中的状态，这个标签有着不同的状态。你可以使用 CSS 去定位或者说针对这些不同的状态进行修饰——下面的 CSS 代码使得没有被访问的链接颜色变为粉色、访问过的链接变为绿色。

```
a:link {
  color: pink;
}

a:visited {
  color: green;
}
```

你可以改变链接被鼠标悬停的时候的样式，例如移除下划线，下面的代码就实现了这个功能。

```
a:hover {
  text-decoration: none;
}
```

在下面的例子中，你可以对超链接的不同状态尝试各种各样的值。我已经编写了一些规则，然而你肯定已经发现粉色看上去太浅以至于不好辨认。——换一个更好的颜色吧。你能将链接变为黑体吗？

我们对鼠标悬停于链接上的情况删除了下划线。你当然可以让超链接在任何情况下都没有下划线。但需要注意的是，对一个实际的站点，需要让浏览者知道“链接是链接”。为了让浏览者注意到一段文字中的某些部分是可点击的，最好保留 link 状态下的下划线。— 这是下划线的本来作用。不管你用 CSS 来做什么，都应当使得变化后的文档看上去更加清晰明了。— 在后面，当我们遇到类似的情况时，我们将适时指出。

**备注：** 在本教程以及整个 MDN 站点中，你会经常看到“无障碍”这个词。“无障碍”一词的意思是，我们的网页应当让每一个访客都能够理解、使用。

你的访客可能在一台使用鼠标和键盘操作的计算机前，也可能正在使用带有触摸屏的手机，或者正在使用屏幕阅读软件读出文档内容，或者他们需要使用更大的字体，或者仅仅使用键盘浏览站点。

一个朴素的 HTML 文档一般来说对任何人都是可以无障碍访问的，当你开始为它添加样式，记得不要破坏这种无障碍。

## [同时使用选择器和选择符](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/First_steps/Getting_started#同时使用选择器和选择符 "Permalink to 同时使用选择器和选择符")

你可以同时使用选择器和选择符。来看一些例子：

```
/* selects any <span> that is inside a <p>, which is inside an <article>  */
article p span { ... }

/* selects any <p> that comes directly after a <ul>, which comes directly after an <h1>  */
h1 + ul + p { ... }
```

你可以将多种类型组合在一起。试试将下面的代码添加到你的代码里：

```
body h1 + p .special {
  color: yellow;
  background-color: black;
  padding: 5px;
}
```

上面的代码为以下元素建立样式：在 `<body>` 之内，紧接在 `<h1>` 后面的 `<p>` 元素的内部，类名为 special。

在我们提供的原始 HTML 文档中，与之符合的元素只有`<span class="special">`.

如果你现在觉得这份代码太复杂了，别担心，一旦你开始编写更多的 CSS 代码，你很快就能找到窍门。

## [选择器](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/First_steps/How_CSS_is_structured#选择器 "Permalink to 选择器")

讲到 CSS 就不得不说到选择器，并且在之前的辅导教程中我们已经列举了一些不同的选择器。为了样式化某些元素，我们会通过选择器来选中 HTML 文档中的这些元素。如果你的样式没有生效，那很可能是你的选择器没有像你想象的那样选中你想要的元素。

每个 CSS 规则都以一个选择器或一组选择器为开始，去告诉浏览器这些规则应该应用到哪些元素上。以下都是有效的选择器或组合选择器的示例。

```
h1
a:link
.manythings
#onething
*
.box p
.box p:first-child
h1, h2, .intro
```

尝试创建一些使用上述选择器的 CSS 规则，并创建一些 HTML 样式。如果您不知道上面的一些语法意味着什么，请尝试在 MDN 上搜索它！

### [专一性](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/First_steps/How_CSS_is_structured#专一性 "Permalink to 专一性")

通常情况下，两个选择器可以选择相同的 HTML 元素。考虑下面的样式表，其中我有一个规则，其中有一个将段落设置为蓝色的 p 选择器，还有一个将选定元素设置为红色的类。

```
.special {
  color: red;
}

p {
  color: blue;
}
```

比方说，在我们的 HTML 文档中，我们有一个带有特殊类的段落。这两条规则都适用，那么谁赢了？你认为我们的段落会变成什么颜色？

```
<p class="special">What color am I?</p>
```

CSS 语言有规则来控制在发生碰撞时哪条规则将获胜——这些规则称为级联规则和专用规则。在下面的代码块中，我们为 p 选择器定义了两个规则，但是段落最后是蓝色的。这是因为将其设置为蓝色的声明将出现在样式表的后面，而稍后的样式将覆盖以前的样式。这就是起作用的级联。

```
p {
  color: red;
}

p {
  color: blue;
}
```

但是，在我们同时使用了类选择器和元素选择器的前一个例子中，类将获胜，使得段落变红——即使它出现在样式表的前面。一个类被描述为比元素选择器更具体，或者具有更多的特异性，所以它获胜了。

自己试试上面的实验——将 HTML 添加到您的实验中，然后将两个 `p{.}` 规则添加到样式表中。接下来，将第一个 `p` 选择器更改为 `.special`，以查看它如何更改样式。

一开始，具体性和层叠的规则看起来有点复杂，一旦你积累了更多的 CSS 知识，就更容易理解了。在我们的级联和继承文章 (将在下一个模块中讨论) 中，我将详细解释这一点，包括如何计算专用性。现在，请记住这是存在的，有时 CSS 可能不会像您预期的那样应用，因为样式表中的其他内容具有更高的特异性。确定一个元素可以适用不止一个规则是解决这些问题的第一步

### [函数](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/First_steps/How_CSS_is_structured#函数 "Permalink to 函数")

虽然大多数值是相对简单的关键字或数值，但也有一些可能的值以函数的形式出现。一个例子是 calc() 函数。这个函数允许您在 CSS 中进行简单的计算，例如：

```
<div class="outer"><div class="box">The inner box is 90% - 30px.</div></div>
```

```
.outer {
  border: 5px solid black;
}

.box {
padding: 10px;
width: calc(90% - 30px);
background-color: rebeccapurple;
color: white;
}
```

如下所示：

一个函数由函数名和一些括号组成，其中放置了该函数的允许值。在上面的 `calc()` 示例中，我要求此框的宽度为包含块宽度的 90%，减去 30 像素。这不是我可以提前计算的东西，只是在 CSS 中输入值，因为我不知道 90% 会是什么。与所有值一样，MDN 上的相关页面将有使用示例，这样您就可以看到函数是如何工作的。

另一个例子是[`<transform>`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/transform), 例如 `rotate()`.

```
<div class="box"></div>
```

```
.box {
  margin: 30px;
  width: 100px;
  height: 100px;
  background-color: rebeccapurple;
  transform: rotate(0.8turn)
}
```

以上代码的输出如下所示：

**尝试查找一下属性的不同值，并编写将他们应用于不同 HTML 元素的 CSS 规则：**

-   **[`transform`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/transform)**
-   **[`background-image`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/background-image), in particular gradient values**
-   **[`color`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/color), in particular rgb/rgba/hsl/hsla values**

## [@规则](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/First_steps/How_CSS_is_structured#规则 "Permalink to @规则")

到目前为止，我们还没有遇到 [`@rules`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/At-rule) (发音为 "at-rules")。这是一些特殊的规则，为 CSS 提供了一些关于如何表现的指导。有些 `@rules` 规则很简单，有规则名和值。例如，要将额外的样式表导入主 CSS 样式表，可以使用 `@import`:

```
@import 'styles2.css';
```

您将遇到的最常见的 @rule 之一是 `@media`，它允许您使用[媒体查询](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Media_Queries)来应用 CSS，仅当某些条件成立 (例如，当屏幕分辨率高于某一数量，或屏幕宽度大于某一宽度时)。

在下面的 CSS 中，我们将给 `<body>` 元素一个粉红色的背景色。但是，我们随后使用 @media 创建样式表的一个部分，该部分仅适用于视口大于 30em 的浏览器。如果浏览器的宽度大于 30em，则背景色将为蓝色。

```
body {
  background-color: pink;
}

@media (min-width: 30em) {
  body {
    background-color: blue;
  }
}
```

在这些教程中，你将遇到一些其他的 `@rules` 规则

**查看是否可以将媒体查询添加到 CSS 中，该查询将根据视口宽度更改样式。更改浏览器窗口的宽度以查看结果。**

## [速记属性](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/First_steps/How_CSS_is_structured#速记属性 "Permalink to 速记属性")

一些属性，如 [`font`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/font), [`background`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/background), [`padding`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/padding), [`border`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/border), and [`margin`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/margin) 等属性称为速记属性--这是因为它们允许您在一行中设置多个属性值，从而节省时间并使代码更整洁。

例如，这一行代码：

```
/* In 4-value shorthands like padding and margin, the values are applied
   in the order top, right, bottom, left (clockwise from the top). There are also other
   shorthand types, for example 2-value shorthands, which set padding/margin
   for top/bottom, then left/right */
padding: 10px 15px 15px 5px;
```

与这四行代码是等价的：

```
padding-top: 10px;
padding-right: 15px;
padding-bottom: 15px;
padding-left: 5px;
```

这一行：

```
background: red url(bg-graphic.png) 10px 10px repeat-x fixed;
```

与这五行代码是等价的：

```
background-color: red;
background-image: url(bg-graphic.png);
background-position: 10px 10px;
background-repeat: repeat-x;
background-attachment: fixed;
```

我们现在不打算详尽地教授这些内容——在后面的课程中，您将看到许多例子，我们建议您查找 CSS 参考中的速记属性名称，以查找更多内容。

尝试将上述声明添加到 CSS 中，看看它如何影响 HTML 的样式。试着尝试一些不同的属性值。

**警告：** 虽然速记经常允许您忽略值，但它们会将不包含的任何值重置为它们的初始值。这确保使用了一组合理的值。但是，如果您期望速记只更改传入的值，这可能会使您感到困惑。

## [当浏览器遇到无法解析的 CSS 代码会发生什么](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/First_steps/How_CSS_works#当浏览器遇到无法解析的_css_代码会发生什么 "Permalink to 当浏览器遇到无法解析的 CSS 代码会发生什么")

在[之前的文章中](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/First_steps/What_is_CSS#%E6%B5%8F%E8%A7%88%E5%99%A8%E6%94%AF%E6%8C%81)我们提到了浏览器并不会同时实现所有的新 CSS，此外很多人也不会使用最新版本的浏览器。鉴于 CSS 一直不断的开发，因此领先于浏览器可以识别的范围，那么你也许会好奇当浏览器遇到无法解析的 CSS 选择器或声明的时候会发生什么呢？

答案就是浏览器什么也不会做，继续解析下一个 CSS 样式！

如果一个浏览器在解析你所书写的 CSS 规则的过程中遇到了无法理解的属性或者值，它会忽略这些并继续解析下面的 CSS 声明。在你书写了错误的 CSS 代码（或者误拼写），又或者当浏览器遇到对于它来说很新的还没有支持的 CSS 代码的时候上述的情况同样会发生（直接忽略）。

相似的，当浏览器遇到无法解析的选择器的时候，他会直接忽略整个选择器规则，然后解析下一个 CSS 选择器。

在下面的案例中，我使用会导致属性错误的英式拼写来书写"color"，所以我的段落没有被渲染成蓝色，而其他的 CSS 代码会正常执行，只有错误的部分会被忽略。

```
<p>I want this text to be large, bold and blue.</p>
```

```
p {
  font-weight: bold;
  colour: blue; /* incorrect spelling of the color property */
  font-size: 200%;
}
```

这样做好处多多，代表着你使用最新的 CSS 优化的过程中浏览器遇到无法解析的规则也不会报错。当你为一个元素指定多个 CSS 样式的时候，浏览器会加载样式表中的最后的 CSS 代码进行渲染（样式表，优先级等请读者自行了解），也正因为如此，你可以为同一个元素指定多个 CSS 样式来解决有些浏览器不兼容新特性的问题（比如指定两个`width`）。

这一特点在你想使用一个很新的 CSS 特性但是不是所有浏览器都支持的时候（浏览器兼容）非常有用，举例来说，一些老的浏览器不接收`calc()`(calculate 的缩写，CSS3 新增，为元素指定动态宽度、长度等，注意此处的动态是计算之后得一个值) 作为一个值。我可能使用它结合像素为一个元素设置了动态宽度（如下），老式的浏览器由于无法解析忽略这一行；新式的浏览器则会把这一行解析成像素值，并且覆盖第一行指定的宽度。

```
.box {
  width: 500px;
  width: calc(100% - 50px);
}
```

后面的课程我们会讨论更多关于浏览器兼容的问题。

# CSS

### [层叠](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#层叠 "Permalink to 层叠")

样式表[**层叠**](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Cascade)——简单的说，就是 CSS 规则的顺序很重要；当应用两条同级别的规则到一个元素的时候，写在后面的就是实际使用的规则。

下面的示例中，我们有两个关于 `<h1>` 的规则。`<h1>` 最后显示蓝色——这两个规则来自同一个源，且具有相同的元素选择器，有相同的优先级，所以顺序在最后的生效。

### [优先级](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#优先级 "Permalink to 优先级")

浏览器是根据[优先级](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Specificity)来决定当多个规则有不同选择器对应相同的元素的时候需要使用哪个规则。它基本上是一个衡量选择器具体选择哪些区域的尺度：

-   一个元素选择器不是很具体，则会选择页面上该类型的所有元素，所以它的优先级就会低一些。
-   一个类选择器稍微具体点，则会选择该页面中有特定 `class` 属性值的元素，所以它的优先级就要高一点。

下面我们再来介绍两个适用于 `<h1>` 的规则。下面的 `<h1>` 最后会显示红色——类选择器 `main-heading` 有更高的优先级，因此就会被应用——即使元素选择器顺序在它后面。

### [继承](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#继承 "Permalink to 继承")

继承也需要在上下文中去理解——一些设置在父元素上的 CSS 属性是可以被子元素继承的，有些则不能。

举一个例子，如果你设置一个元素的 `color` 和 `font-family`，每个在里面的元素也都会有相同的属性，除非你直接在元素上设置属性。

#### [理解继承](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#理解继承 "Permalink to 理解继承")

我们从继承开始。下面的例子中我们有一个 [`<ul>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/ul) 元素，里面有两个无序列表。我们已经给 `<ul>` 设置了边框（border）、内边距（padding）和字体颜色。

`color` 属性是一个继承属性。因此，`color` 属性应用在直接子元素和其后代——直接子元素 `<li>` 和第一个嵌套列表中的子项。然后添加了一个 `special` 类到第二个嵌套列表，其中使用了不同的颜色。然后通过它的子元素继承。

像 `width`（上面提到的）、`margin`、`padding` 和 `border` 不会被继承。如果 border 可以被继承，每个列表和列表项都会获得一个边框——可能就不是我们想要的结果！

尽管每个 CSS 属性页都列出了属性是否被继承，但我们通常可以通过常识来判断哪些属性属于默认继承。

#### [控制继承](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#控制继承 "Permalink to 控制继承")

CSS 为控制继承提供了五个特殊的通用属性值。每个 CSS 属性都接收这些值。

[`inherit`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/inherit)

设置该属性会使子元素属性和父元素相同。实际上，就是“开启继承”。

[`initial`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/initial)

将应用于选定元素的属性值设置为该属性的[初始值](https://developer.mozilla.org/zh-CN/docs/Web/CSS/initial_value)。

[`revert` (en-US)](https://developer.mozilla.org/en-US/docs/Web/CSS/revert "Currently only available in English (US)")

将应用于选定元素的属性值重置为浏览器的默认样式，而不是应用于该属性的默认值。在许多情况下，此值的作用类似于 [`unset`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/unset)。

[`revert-layer` (en-US)](https://developer.mozilla.org/en-US/docs/Web/CSS/revert-layer "Currently only available in English (US)")

将应用于选定元素的属性值重置为在上一个[层叠层](https://developer.mozilla.org/zh-CN/docs/Web/CSS/@layer)中建立的值。

[`unset`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/unset)

将属性重置为自然值，也就是如果属性是自然继承那么就是 `inherit`，否则和 `initial` 一样

**备注：** 见 [CSS 层叠](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Cascade) 中的 [CSS 声明的源](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Cascade#css_声明的源) 有更多信息和具体是怎么工作的。

我们可以查看一个链接列表来探索这些值是如何运作的。在下面的实例中，你可以通过修改 CSS 来查看它们的功能，写代码是掌握 HTML 和 CSS 最好的办法。

示例：

1.  第二个列表项应用了类 `my-class-1`。它设置了内部元素来继承属性。如果你删除这个类，它会如何改变链接的颜色？
2.  你知道为什么第三个和第四个链接会是这样的颜色？第三个链接设置了 `initial`，这意味着它使用了属性的初始值（在本例中为黑色），而不是链接的浏览器默认样式的蓝色。第四个设置了 `unset`，这意味着链接文本会使用其父元素的颜色——绿色。
3.  如果你为 `<a>` 元素定义新的颜色（例如：`a { color: red; }`），哪些链接会改变颜色？
4.  阅读下一节有关重置所有属性的内容后，回到这里，并将 `color` 属性改为 `all` 属性。注意第二个链接是怎么出现在新的一行中，还带有一个无序列表的符号的。你认为继承了哪些属性。

#### [重设所有属性值](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#重设所有属性值 "Permalink to 重设所有属性值")

CSS 的简写属性 [`all`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/all) 可以用于同时将这些继承值中的一个应用于（几乎）所有属性。它的值可以是其中任意一个（`inherit`、`initial`、`unset` 或 `revert`）。这是一种撤销对样式所做更改的简便方法，以便回到之前已知的起点。

下面的示例中有两个块级引用元素。第一个用元素本身的样式，第二个设置 `all` 为 `unset`

试着将 `all` 改成其它可用的值然后观察有什么不一样。

`all` 子元素全元素控制

原本是子元素单一元素控制

## [理解层叠](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#理解层叠 "Permalink to 理解层叠")

我们现在明白了为什么嵌套在 HTML 结构中的段落和应用于正文中的 CSS 颜色相同，从入门课程中，我们了解了如何将文档中的任何修改应用于某个对象的 CSS，无论是把 CSS 指定某个元素还是创建一个类。现在，我们将要了解层叠如何定义在不止一个元素的时候怎么应用 CSS 规则。

有三个因素需要考虑，根据重要性排序如下，后面的更重要：

1.  **资源顺序**
2.  **优先级**
3.  **重要程度**

我们从上往下看，看看浏览器是如何决定该应用哪个 CSS 规则的。

### [资源顺序](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#资源顺序 "Permalink to 资源顺序")

我们已经看到了顺序对于层叠的重要性。如果你有超过一条规则，而且都是相同的权重，那么最后面的规则会应用。可以理解为后面的规则覆盖前面的规则，直到最后一个开始设置样式。

资源顺序仅在规则的优先级相同时才体现出来，下面让我们看一下优先级：

### [优先级](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#优先级_2 "Permalink to 优先级")

你会发现在一些情况下，有些规则在最后出现，但是却应用了前面的具有冲突的规则。这是因为前面的有更高的**优先级**——它范围更小，因此浏览器就把它选择为元素的样式。

就像前面看到的，类选择器的权重大于元素选择器，因此类上定义的属性将覆盖应用于元素上的属性。

这里需要注意虽然我们考虑的是选择器，以及应用在选中对象上的规则，但不会覆盖所有规则，只覆盖相同的属性。

这样可以避免重复的 CSS。一种常见的做法是给基本元素定义通用样式，然后给不同的元素创建对应的类。举个例子，在下面的样式中我给 2 级标题定义了通用样式，然后创建了一些类只修改部分属性的值。最初定义的值应用于所有标题，然后更具体的值通过对应类来实现。

现在让我们来看看浏览器如何计算优先级。我们已经知道一个元素选择器比类选择器的优先级更低，会被其覆盖。本质上，不同类型的选择器有不同的分数值，把这些分数相加就得到特定选择器的权重，然后就可以进行匹配。

一个选择器的优先级可以说是由三个不同的值（或分量）相加，可以认为是百（ID）十（类）个（元素）——三位数的三个位数：

-   **ID**：选择器中包含 ID 选择器则百位得一分。
-   **类**：选择器中包含类选择器、属性选择器或者伪类则十位得一分。
-   **元素**：选择器中包含元素、伪元素选择器则个位得一分。

**备注：** 通用选择器（[`*`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Universal_selectors)）、组合符（`+`、`>`、`~`、' '）和调整优先级的选择器（[`:where()`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:where)）不会影响优先级。

***就是说这些玩意没有优先级晓得吧***

否定（[`:not()`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:not)）和任意匹配（[`:is()`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:is)）伪类本身对优先级没有影响，但它们的参数则会带来影响。参数中，对优先级算法有贡献的参数的优先级的最大值将作为该伪类选择器的优先级。

下面有几个单独的例子，有空可以看看。试着思考下，理解为什么优先级是这样定的。我们还没有深入介绍选择器，不过你可以在 MDN 的[选择器参考页面](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_Selectors)找到每个选择器的详细信息。


|选择器|ID|类|元素|优先级|
|---|---|---|---|-----|
|`h1`|0|0|1|0-0-1|
|`h1 + p::first-letter`|0|0|3|0-0-3|
|`li > a[href*="en-US"] > .inline-warning`|0|2|2|0-2-2|
|`#identifier`|1|0|0|1-0-0|
|`button:not(#mainBtn, .cta)`|1|0|1|1-0-1|

***这个没有进位这个没有进位这个没有进位这个没有进位这个没有进位这个没有进位***

***这个没有逗号这个没有逗号这个没有逗号这个没有逗号这个没有逗号这个没有逗号***

在我们继续之前，先看看这个示例。

这里发生了什么？首先，我们先看看最上面的选择器规则，你会发现，我们已经把优先级计算出来放在最前面的注释里。

-   前面两个选择器都是链接背景颜色的样式——第二个赢了使得背景变成蓝色，因为它多了一个 ID 选择器：优先级 2-0-1 vs. 1-0-1。
-   第三四个选择器都是链接文本颜色样式——后者赢了使得文本变成白色，因为它虽然少一个元素选择器，但是多了一个类选择器。所以优先级是 1-1-3 vs. 1-0-4。
-   第 5 到 7 个选择器都是鼠标悬停时链接边框样式。第六个显然输给了第五个，优先级是 0-2-3 vs. 0-2-4——少了个元素选择器。第七个，比第五第六都高——子选择器数量相同，但是有一个元素选择器变成类选择器。所以最后优先级是 0-3-3 vs. 0-2-3 和 0-2-4。

**备注：** 每一个选择器类编都有它自己的优先级等级，它们不会被具有较低优先级的选择器覆盖。例如，权重为_一百万_的**类**选择器不会覆盖权重为_一_的 **ID** 选择器。

评估优先级的最佳方法是对不同的优先级等级单独进行评分，并从最高的等级开始，必要时再计算低优先级等级的权重。即，仅当某一列的优先级权重相同时，你才需要评估下一列；否则，你可以直接忽略低等级的选择器，因为它们无法覆盖高优先级等级的选择器。

### [内联样式](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#内联样式 "Permalink to 内联样式")

内联样式，即 [`style`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Global_attributes#style) 属性内的样式声明，优先于所有普通的样式，无论其优先级如何。这样的声明没有选择器，但它们的优先级可以理解为 1-0-0-0；即无论选择器中有多少个 ID，它总是比其它任何优先级的权重都要高。

### [!important](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#!important "Permalink to !important")

有一个特殊的 CSS 可以用来覆盖所有上面所有优先级计算，不过需要很小心的使用——`!important`。用于修改特定属性的值，能够覆盖普通规则的层叠。

```
p {      		
	background: green !important;
}
```

**备注：** 了解 `!important` 是为了在阅读别人代码的时候知道有什么作用。**但是，强烈建议除了非常情况不要使用它。**`!important` 改变了层叠的常规工作方式，它会使调试 CSS 问题非常困难，特别是在大型样式表中。

看看这个示例，有两个段落，其中一个有 ID。

让我们看看会发生什么——如果有什么疑问，试着删除一些属性：

1.  你会发现第三个规则 [`color`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/color) 和 [`padding`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/padding) 的值被应用了，但是 [`background-color`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/background-color) 没有。为什么？应该三个都应用，因为顺序规则是后面覆盖前面。
2.  无论如何，上面的规则赢了，因为类选择器比元素选择器有更高的优先级。
3.  两个元素都有 `better` [`class`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Global_attributes#class)，但是第二个有 [`id`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Global_attributes#id) 。因为 ID 选择器比类选择器优先级更高（一个页面只能有一个独特的 ID，但是很多元素都有相同的类——ID 对于目标非常独特），红色背景和 1px 黑色边框应该都被应用到第二个元素，第一个元素应该是灰色背景和 no border，根据类选择器。
4.  第二个元素有红色背景但是没有边框。为什么？因为 `!important` 声明在第二条规则里——在 `border: none` 后面，说明即使计算优先级低，这个属性也使用这个值。

**备注：** 覆盖 `!important` 唯一的办法就是另一个 `!important` 具有相同_优先级_而且顺序靠后，或者更高优先级。

在一种情况下，你可能不得不使用它：当你不能编辑核心的 CSS 模块，不能用任何其他方式覆盖，而你又真的想要覆盖一个样式时。但说真的，如果可以避免的话就不要用它。

***不要用不要用不要用不要用不要用不要用不要用不要用不要用不要用不要用不要用不要用不要用***

## [CSS 位置的影响](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#css_位置的影响 "Permalink to CSS 位置的影响")

最后，也很有用，CSS 声明的优先级取决于定义它的样式表和级联层。

它让用户可以设置自定义样式表来覆盖开发人员定义的样式。例如用户可能视力受损，并想在所有网页上设置两倍的正常字体大小，以便更容易进行阅读。

也可以在级联层中声明开发人员定义的样式：你可以让非分层样式覆盖分层样式，或者你可以让后面的层中声明的样式覆盖先前的层中声明的样式。例如，作为开发人员，你可能无法编辑第三方的样式表，但你可以将外部的样式表导入级联层中，以便你自己的样式可以轻松地覆盖导入的样式，无需担心第三方选择器的优先级。

### [覆盖声明的顺序](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance#覆盖声明的顺序 "Permalink to 覆盖声明的顺序")

相互冲突的声明将按以下顺序应用，后一种声明将覆盖前一种声明：

1.  用户代理样式表中的声明（例如，浏览器的默认样式，在没有设置其他样式时使用）。
2.  用户样式表中的常规声明（由用户设置的自定义样式）。
3.  作者样式表中的常规声明（这些是我们 web 开发人员设置的样式）。
4.  作者样式表中的 `!important` 声明
5.  用户样式表中的 `!important` 声明
6.  用户代理样式表中的 `!important` 声明

	**备注：** 标记为 `!important` 的样式的优先级顺序是颠倒的。web 开发人员的样式表覆盖用户的样式表是有意义的，因此设计可以按预期进行，但是有时用户有充足的理由覆盖 web 开发人员的样式，正如上面提到的——这可以通过在他们的规则中使用 `!important` 来实现。

### [@layer](https://developer.mozilla.org/zh-CN/docs/Web/CSS/@layer)

这玩意好用极了

但需注意的是，***这些层里面还是按照原来的优先级排列***

你可以整个

- 命名层

- 匿名层

- 没有层

越往后优先级越大

你也可以创建带命名的级联层，但不指定任何样式。例如，单一的命名层：

```
@layer utilities
```

这后面是直接加个大括号写CSS的

或者，多个命名层也可以被同时定义。例如：

```
@layer theme, layout, utilities;
```

后面有冒号

这样很有用，这样你的命名层们就按照这个方式划分优先级，越往后优先级越大

一个级联层同样可以通过 [`@import`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/@import) 来创建，规则存在于被引入的样式表内：

```
@import(utilities.css) layer(utilities);
```

### [嵌套层](https://developer.mozilla.org/zh-CN/docs/Web/CSS/@layer#嵌套层 "Permalink to 嵌套层")

级联层允许嵌套，例如：

```
@layer framework {
  @layer layout {

  }
}
```

向 `layout` 层内部的 `framework` 层附加规则，只需用 `.` 连接这两层。

```
@layer framework.layout {
  p {
    margin-block: 1rem;
  }
}
```

## [选择器列表](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors#选择器列表 "Permalink to 选择器列表")

空格可以在逗号前或后，你可能还会发现如果每个选择器都另起一行，会更好读些。

```
h1,
.special {
  color: blue;
}
```

当你使用选择器列表时，如果任何一个选择器无效 (存在语法错误)，那么整条规则都会被忽略。

在下面的示例中，无效的 class 选择器会被忽略，而`h1`选择器仍会被样式化。

```
h1 {
  color: blue;
}

..special {
  color: blue;
}
```

但是在被组合起来以后，整个规则都会失效，无论是`h1`还是这个 class 都不会被样式化。

```
h1, ..special {
  color: blue;
}
```

## [选择器的种类](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors#选择器的种类 "Permalink to 选择器的种类")

有几组不同的选择器，知道了需要哪种选择器，你会更容易正确使用它们。在本文的子篇中，我们将会来更详细地看下不同种类的选择器。

### [类型、类和 ID 选择器](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors#类型、类和_id_选择器 "Permalink to 类型、类和 ID 选择器")

这个选择器组，第一个是指向了所有 HTML 元素 `<h1>`。

```
h1 { }
```

它也包含了一个 class 的选择器：

```
.box { }
```

亦或，一个 id 选择器：

```
#unique { }
```

### [标签属性选择器](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors#标签属性选择器 "Permalink to 标签属性选择器")

这组选择器根据一个元素上的某个标签的属性的存在以选择元素的不同方式：

```
a[title] { }
```

或者根据一个有特定值的标签属性是否存在来选择：

```
a[href="https://example.com"] { }
```

### [伪类与伪元素](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors#伪类与伪元素 "Permalink to 伪类与伪元素")

这组选择器包含了伪类，用来样式化一个元素的特定状态。例如`:hover`伪类会在鼠标指针悬浮到一个元素上的时候选择这个元素：

```
a:hover { }
```

它还可以包含了伪元素，选择一个元素的某个部分而不是元素自己。例如，`::first-line`是会选择一个元素（下面的情况中是`<p>`）中的第一行，类似`<span>`包在了第一个被格式化的行外面，然后选择这个`<span>`。

```
p::first-line { }
```

### [运算符](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors#运算符 "Permalink to 运算符")

最后一组选择器可以将其他选择器组合起来，更复杂的选择元素。下面的示例用运算符（`>`）选择了`<article>`元素的初代子元素。

```
article > p { }
```

## [选择器参考表](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors#选择器参考表 "Permalink to 选择器参考表")

下面的表格让你可以浏览你可以用的选择器，还有本指南中教你如何使用每种选择器的页面的链接。我还加上了一个能查看浏览器对每个选择器的支持信息的 MDN 页面链接。你可以把这个作为回头的参考，在你以后需要查询文献中提到的选择器的时候，或者是在你广义上实验 CSS 的时候。

|选择器|示例|
|---|---|
|[类型选择器](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Type_selectors)|`h1 { }`|
|[通配选择器](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Universal_selectors)|`* { }`|
|[类选择器](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Class_selectors)|`.box { }`|
|[ID 选择器](https://developer.mozilla.org/zh-CN/docs/Web/CSS/ID_selectors)|`#unique { }`|
|[标签属性选择器](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Attribute_selectors)|`a[title] { }`|
|[伪类选择器](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Pseudo-classes)|`p:first-child { }`|
|[伪元素选择器](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Pseudo-elements)|`p::first-line { }`|
|[后代选择器](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Descendant_combinator)|`article p`|
|[子代选择器](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Child_combinator)|`article > p`|
|[相邻兄弟选择器](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Adjacent_sibling_combinator)|`h1 + p`|
|[通用兄弟选择器](https://developer.mozilla.org/zh-CN/docs/Web/CSS/General_sibling_combinator)|`h1 ~ p`|

## [全局选择器](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Type_Class_and_ID_Selectors#全局选择器 "Permalink to 全局选择器")

全局选择器，是由一个星号（`*`）代指的，它选中了文档中的所有内容（或者是父元素中的所有内容，比如，它紧随在其他元素以及邻代运算符之后的时候）。下面的示例中，我们已经用全局选择器，移去了所有元素上的外边距。这就是说，和浏览器以外边距隔开标题和段的方式默认加上的样式不同的是，每个物件都紧紧地挨在一起，我们不能那么容易就看清楚不同的段。

这种行为有时能在“重置样式表”中看到，其中所有浏览器所做的样式化都会被忽略。这些一度很受欢迎，但是把所有的样式化忽略掉的话，通常就是指，你必须做把这些样式带回来的工作！因此我们应小心使用全局选择器，以处理诸如下面所述之类的很特殊的情况。

### [使用全局选择器，让选择器更易读](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Type_Class_and_ID_Selectors#使用全局选择器，让选择器更易读 "Permalink to 使用全局选择器，让选择器更易读")

全局选择器的一种用法是让选择器更易读，更明显地表明它们的作用。例如，如果我想选中任何`<article>`元素的第一子元素，不论它是什么元素，都给它加粗，我可以将[`:first-child`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:first-child)选择器（我们将会在[伪类和伪元素](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Pseudo-classes_and_pseudo-elements)课中进一步了解）用作`<article>`元素选择器的一个后代选择器：

```
article :first-child {

}
```

但是这会和`article:first-child`混淆，而后者选择了作为其他元素的第一子元素的`<article>`元素。

为了避免这种混淆，我们可以向`:first-child`选择器加入全局选择器，这样选择器所做的事情很容易就能看懂。选择器正选中`<article>`元素的_任何_第一子元素：

```
article *:first-child {

}
```

来解释一下，一个选择器 空格 后面的就是子选择器，也就是 `article :first-child`

但就空了个格

于是有人搞个星号，好判断，对人身体好，要不看看标题是什么？

`article:first-child` 就是没有空格那个指的就是“`<article>` 如果作为第一个子属性必须被选择”

### 使用全局选择器来搞点你不知道的东西

有时候，你并不知道自己会选择什么

比如说关系选择器

```
body article p
article > p
p + img
p ~ img
```

如果想的话，还可以这样做

```
body article *
body * p
article > *
p + *
p ~ *
```

## [类选择器](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Type_Class_and_ID_Selectors#类选择器 "Permalink to 类选择器")

类选择器以一个句点（`.`）开头，会选择文档中应用了这个类的所有物件。在下面的实时示例中，我们已经建立了一个名为`.highlight`的类，把它应用到了我的文档中的几个地方。所有包含此类的元素都被高亮了。

```
.highlight {
    background-color: yellow;
}
```

### [指向特定元素的类](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Type_Class_and_ID_Selectors#指向特定元素的类 "Permalink to 指向特定元素的类")

你能建立一个指向应用一个类的特定元素。在下一个示例里面，我们将会用不同方式高亮一个带有`highlight`类的`<span>`和带有 `highlight`类的`<h1>`标题。我们通过使用附加了类的欲选元素的选择器做到这点，其间没有空格。

```
span.highlight {
    background-color: yellow;
}

h1.highlight {
    background-color: pink;
}
```

这种方式使 CSS 没那么可复用，因为类现在只会应用到那个特定元素，在认为规则也该应用到其他元素的时候，你会需要另外加上一个选择器。

### [多个类被应用的时候指向一个元素](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Type_Class_and_ID_Selectors#多个类被应用的时候指向一个元素 "Permalink to 多个类被应用的时候指向一个元素")

你能对一个元素应用多个类，然后分别指向它们，或者仅仅在选择器中存在所有这些类的时候选择这一元素。在你的站点上，构建可以以不同方式组合起来的组件的时候，这会有用。

在下面的示例中，有一个包含了一条笔记的`<div>`。灰色的边框在盒子带有`notebox`类的时候应用。如果它还有一个`warning`或是`danger`类，我们改变[`border-color`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/border-color)。

为了告诉浏览器我们只想匹配带有所有这些类的元素，我们可以将这些类不加空格地连成一串。

```
.notebox {
  border: 4px solid #666;
  padding: .5em;
}

.notebox.warning {
  border-color: orange;
  font-weight: bold;
}

.notebox.danger {
  border-color: red;
  font-weight: bold;
}
```

```
<div class="notebox">
    This is an informational note.
</div>

<div class="notebox warning">
    This note shows a warning.
</div>

<div class="notebox danger">
    This note shows danger!
</div>

<div class="danger">
    This won't get styled — it also needs to have the notebox class
</div>
```

## [ID 选择器](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Type_Class_and_ID_Selectors#id_选择器 "Permalink to ID 选择器")

ID 选择器开头为`#`而非句点，不过基本上和类选择器是同种用法。可是在一篇文档中，一个 ID 只会用到一次。它能选中设定了`id`的元素，你可以在 ID 前面加上类型选择器，只指向元素和 ID 都匹配的类。在下面的示例里，你可以看看这两种用法。

```
#one {
    background-color: yellow;
}

h1#heading {
    color: rebeccapurple;
}
```

```
<h1 id="heading">ID selector</h1>
<p>Veggies es bonus vobis, proinde vos postulo essum magis kohlrabi welsh onion daikon amaranth tatsoi tomatillo
    melon azuki bean garlic.</p>

<p id="one">Gumbo beet greens corn soko <strong>endive</strong> gumbo gourd. Parsley shallot courgette tatsoi pea sprouts fava bean collard
    greens dandelion okra wakame tomato. Dandelion cucumber earthnut pea peanut soko zucchini.</p>
```

**备注：** 正如我们在和特定性相关的课里面学到的那样，ID 所指特定，会优先于大多数其他选择器。所以很难处理它们。大多数情况下，给一个元素加个类，而不是使用 ID，会更好。不过要是 ID 是唯一一种指定这个元素的方式的话——也许是因为你没法访问标记标记因此不能编辑——这种方式可行。

## [存否和值选择器](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Attribute_selectors#存否和值选择器 "Permalink to 存否和值选择器")

这些选择器允许基于一个元素自身是否存在（例如`href`）或者基于各式不同的按属性值的匹配，来选取元素。

|选择器|示例|描述|
|---|---|---|
|`[attr]`|`a[title]`|匹配带有一个名为*attr*的属性的元素——方括号里的值。|
|`[attr=value]`|`a[href="https://example.com"]`|匹配带有一个名为*attr*的属性的元素，其值正为*value*——引号中的字符串。|
|`[attr~=value]`|`p[class~="special"]`|匹配带有一个名为*attr*的属性的元素，其值正为*value*，或者匹配带有一个*attr*属性的元素，其值有一个或者更多，至少有一个和*value*匹配。<br><br>注意，在一列中的好几个值，是用空格隔开的。|
|`[attr\|=value]`|`div[lang\|="zh"]`|匹配带有一个名为*attr*的属性的元素，其值可正为*value*，或者开始为*value*，后面紧随着一个连字符。|

纠正一下，最后一行是`[attr|=value]`，`div[lang|="zh"]`，喵的黑曜石把中间这俩竖杠认成表格了

下面的示例中，你可以看到这些选择器是怎样使用的。

-   使用`li[class]`，我们就能匹配任何有 class 属性的选择器。
- 
- `li[class="a"]`匹配带有一个`a`类的选择器

```
li[class]
li[class="a"]

li[apple]
```

```
<ul>
	<li class="a">Item 2</li>
	
    <li apple class="a b">Item 3</li>
</ul>
```

***没错就是看你标签里有什么

***必须连在一起***

-   `li[class~="a"]`会匹配一个`a`类，不过也可以匹配一列用空格分开、包含`a`类的值

```
li[class~="a"]
li[class~="b"]

li[apple~="apple"]
```

```
<ul>
	<li class="a">Item 2</li>
	
    <li apple class="a b">Item 3</li>
</ul>
```

***属性值只要有就可以了***

***但你加一个字母或连在起一都不行***

-   `li[class~="a"]`会匹配一个`a`类，不过也可以匹配一列用空格分开、包含`a`类的值

```
li[class~="a"]
li[class~="b"]

li[apple~="apple"]
```

```
<ul>
	<li class="a">Item 2</li>
	<li class="a b">Item 2</li>
	
    <li apple class="apple b">Item 3</li>
</ul>
```

***属性值只要有就可以了***

***但你加一个字母或连在起一都不行***

-   `li[class|="a"]`会匹配一个`a`类，不过也可以匹配一列用空格分开、包含`a`类的值

```
li[class|="a"]

li[apple|="apple"]
```

```
<ul>
	<li class="a">Item 2</li>
	<li class="a-potato">Item a</li>
	
    <li apple class="apple-b">Item 3</li>
</ul>
```

***你要么认真写***

***要么加连字符 `|` 而且我 class什么的 里面的属性值必须为开头***

## [子字符串匹配选择器](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Attribute_selectors#子字符串匹配选择器 "Permalink to 子字符串匹配选择器")

这些选择器让更高级的属性的值的子字符串的匹配变得可行。例如，如果你有`box-warning`和`box-error`类，想把开头为“box-”字符串的每个物件都匹配上的话，你可以用`[class^="box-"]`来把它们两个都选中。

|选择器|示例|描述|
|---|---|---|
|`[attr^=value]`|`li[class^="box-"]`|匹配带有一个名为*attr*的属性的元素，其值开头为*value*子字符串。|
|`[attr$=value]`|`li[class$="-box"]`|匹配带有一个名为*attr*的属性的元素，其值结尾为*value*子字符串|
|`[attr*=value]`|`li[class*="box"]`|匹配带有一个名为*attr*的属性的元素，其值的字符串中的任何地方，至少出现了一次*value*子字符串。|

-   `li[class^="a"]`匹配了任何值开头为`a`的属性

-   `li[class$="a"]`匹配了任何值结尾为`a`的属性

-   `li[class*="a"]`匹配了任何值的字符串中出现了`a`的属性

## [大小写敏感](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Attribute_selectors#大小写敏感 "Permalink to 大小写敏感")

如果你想在大小写不敏感的情况下，匹配属性值的话，你可以在闭合括号之前，使用`i`值。这个标记告诉浏览器，要以大小写不敏感的方式匹配 ASCII 字符。没有了这个标记的话，值会按照文档语言对大小写的处理方式，进行匹配——HTML 中是大小写敏感的。

下面的示例中，第一个选择器将会匹配一个开头为`a`的值，这样它只匹配了第一项，因为另外两项开头是大写的 A。第二个选择器使用了大小写不敏感的标记，于是匹配了所有项。

像这样

```
li[class^="a" i] {
    color: red;
}
```

**备注：** 此外还有一个更加新的 `s` 值，它会强制在上下文的匹配正常为大小写不敏感的时候，强行要求匹配时大小写敏感。不过，在浏览器中它不太受支持，而且在上下文为 HTML 时也没啥用。

于是我有一个问题， `s` 值有什么用？

## [什么是伪类？](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Pseudo-classes_and_pseudo-elements#什么是伪类？ "Permalink to 什么是伪类？")

伪类是选择器的一种，它用于选择处于特定状态的元素，比如当它们是这一类型的第一个元素时，或者是当鼠标指针悬浮在元素上面的时候。它们表现得会像是你向你的文档的某个部分应用了一个类一样，帮你在你的标记文本中减少多余的类，让你的代码更灵活、更易于维护。

伪类就是开头为冒号的关键字：

:pseudo-class-name

### [简单伪类示例](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Pseudo-classes_and_pseudo-elements#简单伪类示例 "Permalink to 简单伪类示例")

让我们看下一个简单的示例。如果我们想要让一篇文章中的第一段变大加粗，可为此段加上一个类，然后为那个类添加 CSS，正如下面的示例展示的这样：

```
类
```

不过，这在维护的时候可能会很恼人——要是文档的头部又加上一段的话呢？我们会需要把这个类挪到新加的这段上。假如我们不加类，我们可以使用[`:first-child`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:first-child)伪类选择器——这将_一直_选中文章中的第一个子元素，我们将不再需要编辑 HTML（编辑 HTML 并不总是可行，也许是因为它是由一个 CMS 生成的）。

所有的伪类以同样的方式实现。它们选中你的文档中处于某种状态的那部分，表现得就像是你已经向你的 HTML 加入类一样。看下 MDN 上的另外几个示例：

-   [`:last-child`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:last-child)
-   [`:only-child`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:only-child)
-   [`:invalid`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:invalid)

### [用户行为伪类](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Pseudo-classes_and_pseudo-elements#用户行为伪类 "Permalink to 用户行为伪类")

一些伪类只会在用户以某种方式和文档交互的时候应用。这些**用户行为伪类**，有时叫做**动态伪类**，表现得就像是一个类在用户和元素交互的时候加到了元素上一样。案例包括：

-   [`:hover`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:hover)——上面提到过，只会在用户将指针挪到元素上的时候才会激活，一般就是链接元素。
-   [`:focus`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:focus)——只会在用户使用键盘控制，选定元素的时候激活。

## [伪元素是啥？](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Pseudo-classes_and_pseudo-elements#伪元素是啥？ "Permalink to 伪元素是啥？")

伪元素以类似方式表现，不过表现得是像你往标记文本中加入全新的 HTML 元素一样，而不是向现有的元素上应用类。伪元素开头为双冒号`::`。

```
::pseudo-element-name
```

 **备注：** 一些早期的伪元素曾使用单冒号的语法，所以你可能会在代码或者示例中看到。现代的浏览器为了保持后向兼容，支持早期的带有单双冒号语法的伪元素。

例如，如果你想选中一段的第一行，你可以把它用一个`<span>`元素包起来，然后使用元素选择器；不过，如果包起来的单词/字符数目长于或者短于父元素的宽度，这样做会失败。由于我们一般不会知道一行能放下多少单词/字符——因为屏幕宽度或者字体大小改变的时候这也会变——通过改变 HTML 的方式来可预测地这么做是不可能的。

`::first-line`伪元素选择器会值得信赖地做到这件事——即使单词/字符的数目改变，它也只会选中第一行。

```
article p::first-line {
    font-size: 120%;
    font-weight: bold;
}   
```

```
<article>
    <p>Veggies es bonus vobis, proinde vos postulo essum magis kohlrabi welsh onion daikon amaranth tatsoi tomatillo melon azuki bean garlic.</p>

    <p>Gumbo beet greens corn soko endive gumbo gourd. Parsley shallot courgette tatsoi pea sprouts fava bean collard greens dandelion okra wakame tomato. Dandelion cucumber earthnut pea peanut soko zucchini.</p>
</article>
```

这表现得就像是`<span>`神奇地包在第一个被格式化的行一样，每当行长改变的时候还会更新。

你可以看到它把两段的第一行都选中了。

理解不了点击标题看原稿事例啊

原来可以嵌入啊，但是是他喵的白色系啊

## [生成带有::before 和::after 的内容](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Pseudo-classes_and_pseudo-elements#生成带有before_和after_的内容 "Permalink to 生成带有::before 和::after 的内容")

有一组特别的伪元素，它们和[`content`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/content)属性一同使用，使用 CSS 将内容插入到你的文档中中。

你能用这些插入一个文本字符串，和在下面的实时示例里那样。试着改变[`content`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/content)属性的文本值，看看输出是怎么改变的。你也能改变`::before`伪元素为`::after`，看到这段文本插入到了元素的末尾而不是开头。

```
.box::before {
    content: "This should show before the other content."
}
```

从 CSS 插入文本字符串，我们并不会在 Web 浏览器上经常这么做，因为对于一些屏幕阅读器来说，文本是不可见的，而且对于未来别人的查找和编辑也不是很方便。

这些伪元素的更推荐的用法是插入一个图标，例如下面的示例加入的一个小箭头，作为一个视觉性的提示，而且我们并不希望屏幕阅读器读出它。

```
box::after {
    content: " ➥"
}   
```

这些伪元素经常用于插入空字符串，其后可以像页面上的其他元素被样式化。

下个示例，我们已经用 `::before`伪元素加入了个空字符串。我们把它设为了`display: block`，以让它可以用 width 和 height 进行样式化。然后我们可以用 CSS 像任何元素那样样式化。你可以摆弄 CSS，改变它的外观和行为。

```
.box::before {
    content: "";
    display: block;
    width: 100px;
    height: 100px;
    background-color: rebeccapurple;
    border: 1px solid black;
}   
```

```
<p class="box">Content in the box in my HTML page.</p>
```

`::before`和`::after`伪元素与`content`属性的共同使用，在 CSS 中被叫做“生成内容”，而且你会见到这种技术被用于完成各种任务。[CSS Arrow Please](http://www.cssarrowplease.com/)网站就是一个著名的示例，它帮你用 CSS 生成一个箭头。在你创建你的箭头的时候看下 CSS，你将会看到实际使用的[`::before`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/::before)和[`::after`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/::after)伪元素。无论什么时候你看到了这些选择器，都要看下[`content`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/content)属性，以了解文档中添加了什么。

可以搞 CSS 动画的说

## [参考节](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Pseudo-classes_and_pseudo-elements#参考节 "Permalink to 参考节")

有很多伪类和伪元素，所以有一个用于参考的列表会有用。下面是列出它们的表格，链接到了 MDN 上它们的参考页。把这作为参考，看看你能选中什么。

***而且，如果就这几个的话，你为什么要区分***

### [伪类](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Pseudo-classes_and_pseudo-elements#伪类 "Permalink to 伪类")

选择器

描述
<br>

[`:active`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:active)

在用户激活（例如点击）元素的时候匹配。
<br>

[`:any-link`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:any-link)

匹配一个链接的`:link`和`:visited`状态。
<br>

[`:blank`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:blank)

匹配空输入值的[`<input>`元素](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/Input)。
<br>

[`:checked`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:checked)

匹配处于选中状态的单选或者复选框。
<br>

[`:current` (en-US)](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API "Currently only available in English (US)")

匹配正在展示的元素，或者其上级元素。
<br>

[`:default`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:default)

匹配一组相似的元素中默认的一个或者更多的 UI 元素。
<br>

[`:dir`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:dir)

基于其方向性（HTML[`dir`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Global_attributes/dir)属性或者 CSS[`direction`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/direction)属性的值）匹配一个元素。
<br>

[`:disabled`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:disabled)

匹配处于关闭状态的用户界面元素
<br>

[`:empty`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:empty)

匹配除了可能存在的空格外，没有子元素的元素。
<br>

[`:enabled`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:enabled)

匹配处于开启状态的用户界面元素。
<br>

[`:first`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:first)

匹配[分页媒体](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Paged_Media)的第一页。
<br>

[`:first-child`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:first-child)

匹配兄弟元素中的第一个元素。
<br>

[`:first-of-type`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:first-of-type)

匹配兄弟元素中第一个某种类型的元素。
<br>

[`:focus`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:focus)

当一个元素有焦点的时候匹配。
<br>

[`:focus-visible`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:focus-visible)

当元素有焦点，且焦点对用户可见的时候匹配。
<br>

[`:focus-within`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:focus-within)

匹配有焦点的元素，以及子代元素有焦点的元素。
<br>

[`:future` (en-US)](https://developer.mozilla.org/en-US/docs/Web/CSS/:future "Currently only available in English (US)")

匹配当前元素之后的元素。
<br>

[`:hover`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:hover)

当用户悬浮到一个元素之上的时候匹配。
<br>

[`:indeterminate`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:indeterminate)

匹配未定态值的 UI 元素，通常为[复选框](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/Input/checkbox)。
<br>

[`:in-range`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:in-range)

用一个区间匹配元素，当值处于区间之内时匹配。
<br>

[`:invalid`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:invalid)

匹配诸如`<input>`的位于不可用状态的元素。
<br>

[`:lang`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:lang)

基于语言（HTML[lang](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Global_attributes/lang)属性的值）匹配元素。
<br>

[`:last-child`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:last-child)

匹配兄弟元素中最末的那个元素。
<br>

[`:last-of-type`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:last-of-type)

匹配兄弟元素中最后一个某种类型的元素。
<br>

[`:left`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:left)

在[分页媒体 (en-US)](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Pages "Currently only available in English (US)")中，匹配左手边的页。
<br>

[`:link`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:link)

匹配未曾访问的链接。
<br>

[`:local-link` (en-US)](https://developer.mozilla.org/en-US/docs/Web/CSS/:local-link "Currently only available in English (US)")

匹配指向和当前文档同一网站页面的链接。
<br>

[`:is()`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:is)

匹配传入的选择器列表中的任何选择器。
<br>

[`:not`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:not)

匹配作为值传入自身的选择器未匹配的物件。
<br>

[`:nth-child`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:nth-child)

匹配一列兄弟元素中的元素——兄弟元素按照_an+b_形式的式子进行匹配（比如 2n+1 匹配元素 1、3、5、7 等。即所有的奇数个）。
<br>

[`:nth-of-type`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:nth-of-type)

匹配某种类型的一列兄弟元素（比如，`<p>`元素）——兄弟元素按照_an+b_形式的式子进行匹配（比如 2n+1 匹配元素 1、3、5、7 等。即所有的奇数个）。
<br>

[`:nth-last-child`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:nth-last-child)

匹配一列兄弟元素，从后往前倒数。兄弟元素按照_an+b_形式的式子进行匹配（比如 2n+1 匹配按照顺序来的最后一个元素，然后往前两个，再往前两个，诸如此类。从后往前数的所有奇数个）。
<br>

[`:nth-last-of-type`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:nth-last-of-type)

匹配某种类型的一列兄弟元素（比如，`<p>`元素），从后往前倒数。兄弟元素按照_an+b_形式的式子进行匹配（比如 2n+1 匹配按照顺序来的最后一个元素，然后往前两个，再往前两个，诸如此类。从后往前数的所有奇数个）。
<br>

[`:only-child`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:only-child)

匹配没有兄弟元素的元素。
<br>

[`:only-of-type`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:only-of-type)

匹配兄弟元素中某类型仅有的元素。
<br>

[`:optional`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:optional)

匹配不是必填的 form 元素。
<br>

[`:out-of-range`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:out-of-range)

按区间匹配元素，当值不在区间内的的时候匹配。
<br>

[`:past` (en-US)](https://developer.mozilla.org/en-US/docs/Web/CSS/:past "Currently only available in English (US)")

匹配当前元素之前的元素。
<br>

[`:placeholder-shown`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:placeholder-shown)

匹配显示占位文字的 input 元素。
<br>

[`:playing` (en-US)](https://developer.mozilla.org/en-US/docs/Web/CSS/:playing "Currently only available in English (US)")

匹配代表音频、视频或者相似的能“播放”或者“暂停”的资源的，且正在“播放”的元素。
<br>

[`:paused` (en-US)](https://developer.mozilla.org/en-US/docs/Web/CSS/:paused "Currently only available in English (US)")

匹配代表音频、视频或者相似的能“播放”或者“暂停”的资源的，且正在“暂停”的元素。
<br>

[`:read-only`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:read-only)

匹配用户不可更改的元素。
<br>

[`:read-write`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:read-write)

匹配用户可更改的元素。
<br>

[`:required`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:required)

匹配必填的 form 元素。
<br>

[`:right`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:right)

在[分页媒体 (en-US)](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Pages "Currently only available in English (US)")中，匹配右手边的页。
<br>

[`:root`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:root)

匹配文档的根元素。
<br>

[`:scope`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:scope)

匹配任何为参考点元素的的元素。
<br>

[`:valid`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:valid)

匹配诸如`<input>`元素的处于可用状态的元素。
<br>

[`:target`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:target)

匹配当前 URL 目标的元素（例如如果它有一个匹配当前[URL 分段](https://en.wikipedia.org/wiki/Fragment_identifier)的元素）。
<br>

[`:visited`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:visited)

匹配已访问链接。
<br>

### [伪元素](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Pseudo-classes_and_pseudo-elements#伪元素 "Permalink to 伪元素")

选择器

描述
<br>


[`::after`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/::after)

匹配出现在原有元素的实际内容之后的一个可样式化元素。
<br>


[`::before`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/::before)

匹配出现在原有元素的实际内容之前的一个可样式化元素。
<br>


[`::first-letter`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/::first-letter)

匹配元素的第一个字母。
<br>


[`::first-line`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/::first-line)

匹配包含此伪元素的元素的第一行。
<br>


[`::grammar-error`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/::grammar-error)

匹配文档中包含了浏览器标记的语法错误的那部分。
<br>


[`::selection`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/::selection)

匹配文档中被选择的那部分。
<br>


[`::spelling-error`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/::spelling-error)

匹配文档中包含了浏览器标记的拼写错误的那部分。
<br>
## [后代选择器](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Combinators#后代选择器 "Permalink to 后代选择器")

后代选择器——典型用单个空格（" "）字符——组合两个选择器，比如，第二个选择器匹配的元素被选择，如果他们有一个祖先（父亲，父亲的父亲，父亲的父亲的父亲，等等）元素匹配第一个选择器。选择器利用后代组合符被称作后代选择器。

```
body article p
```

下面的示例中，我们只会匹配处于带有`.box`类的元素里面的`<p>`元素。

```
.box p
```

也就是说，***只要这个 .box 的后代是个 p，那就必被选择，没有数量限制***

***只要是后代，无论是哪家的都要被选择***

## [子代关系选择器](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Combinators#子代关系选择器 "Permalink to 子代关系选择器")

子代关系选择器是个大于号（`>`），只会在选择器选中直接子元素的时候匹配。继承关系上更远的后代则不会匹配。例如，只选中作为`<article>`的直接子元素的`<p>`元素：

```
article > p
```

下个示例中，我们弄了个有序列表，内嵌于另一个无序列表里面。我用子代关系选择器，只选中为`<ul>`的直接子元素的`<li>`元素，给了它们一个顶端边框。

如果你移去指定子代选择器的 `>` 的话，你最后得到的是后代选择器，所有的`<li>`会有个红色的边框。

```
<ul>
    <li>Unordered item</li>
    <li>Unordered item
        <ol>
            <li>Item 1</li>
            <li>Item 2</li>
        </ol>
    </li>
</ul>
```

`<ul>` 和 `<ol>` 中的 `<li>` 已经不是一家了，虽然是后代，但就不是一家了

***只要是子代，都要被选择，但如果还被嵌了一层就不是一家了***

## [邻接兄弟](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Combinators#邻接兄弟 "Permalink to 邻接兄弟")

邻接兄弟选择器（`+`）用来选中恰好处于另一个在继承关系上同级的元素旁边的物件。例如，选中所有紧随`<p>`元素之后的`<img>`元素：

```
p + img
```

常见的使用场景是，改变紧跟着一个标题的段的某些表现方面，就像是我下面的示例那样。这里我们寻找一个紧挨`<h1>`的段，然后样式化它。

如果你往`<h1>`和`<p>`之间插入其他的某个元素，例如`<h2>`，你将会发现，段落不再与选择器匹配，因而不会应用元素邻接时的前景和背景色。

```
h1 + p {
    font-weight: bold;
    background-color: #333;
    color: #fff;
    padding: .5em;
}   
```

```
<article>
    <h1>A heading</h1>
    <p>Veggies es bonus vobis, proinde vos postulo essum magis kohlrabi welsh onion daikon amaranth tatsoi tomatillo
            melon azuki bean garlic.</p>

    <p>Gumbo beet greens corn soko endive gumbo gourd. Parsley shallot courgette tatsoi pea sprouts fava bean collard
            greens dandelion okra wakame tomato. Dandelion cucumber earthnut pea peanut soko zucchini.</p>
</article>
```

在这种情况下，`<h1>` 后面的 `<p>` 会被选择

但是我们只要在`<h1>` 和 `<p>` 中间加点别的

```
<h1>A heading</h1>
<h2>Potato<h2>
    <p>Veggies es bonus vobis, proinde vos postulo essum magis kohlrabi welsh onion daikon amaranth tatsoi tomatillo
            melon azuki bean garlic.</p>
```

`<h1>` 后面的 `<p>` 将不会被选择

其实这种说法不严谨，应该这样说

***`<h1>` 后面第一个元素不是 `<p>`，`<h1>` 后面第一个元素是 `<h2>`***

***`<h1>` 后面有 `<p>` 但 `<p>` 不是 `<h1>` 后面第一个元素***

那好吧，我们要是想选择这里的 `<h2>` 倒也不用填一个 `h1 + h2`，我们还可以这样填

```
h1 + * {
    font-weight: bold;
    background-color: #333;
    color: #fff;
    padding: .5em;
}   
```

全局选择器好得很

也就是说

***只要是这个元素的后面的第一个元素并符合“要选的元素”，那这个元素必将被选择***

## [通用兄弟](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Combinators#通用兄弟 "Permalink to 通用兄弟")

如果你想选中一个元素的兄弟元素，即使它们不直接相邻，你还是可以使用通用兄弟关系选择器（`~`）。要选中所有的`<p>`元素后*任何地方*的`<img>`元素，我们会这样做：

```
p ~ img
```

在下面的示例中，我们选中了所有的 `<h1>`之后的`<p>`元素，虽然文档中还有个 `<div>`，其后的`<p>`还是被选中了。

```
h1 ~ p {
    font-weight: bold;
    background-color: #333;
    color: #fff;
    padding: .5em;
}
```

```
<article>
    <h1>A heading</h1>
    <p>I am a paragraph.</p>
    <div>I am a div</div>
    <p>I am another paragraph.</p>
</article>
```

上面的两个 `<p>` 都被选择了

我们再次加点别的 `<p>`

```
<article>
	<p>potato</p>
    <h1>A heading</h1>
    <p>I am a paragraph.</p>
    <div><p>apple</p></div>
    <p>I am another paragraph.</p>
</article>
```

我们的 `<p>potato</p>` 和 `<p>apple</p>` 不会被选择

`<p>potato</p>` 是不在后面，`<p>apple</p>` 不是兄弟

***只要在这个元素的后面并符合“要选的元素”，那这个元素必将被选择***

## [使用关系选择器](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors/Combinators#使用关系选择器 "Permalink to 使用关系选择器")

你能用关系选择器，将任何在我们前面的学习过程中学到的选择器组合起来，选出你的文档中的一部分。例如如果我们想选中为`<ul>`的直接子元素的带有“a”类的列表项的话，我可以用下面的代码。

```
ul > li[class="a"]  {  }
```

不过，建立一长列选中你的文档中很明确的部分的选择器的时候，小心一些。这些 CSS 规则难以复用，因为你让选择器在表示标记文本中的元素的相对位置上过于明确。

建立简单的一个类，然后把它应用到有需求的元素上，经常会是更好的做法。不过话说回来，如果你需要让你的文档变换一下样式，但是没法编辑 HTML（也许是因为它由 CMS 生成）的话，你的关系选择器的知识会派上用场。

***还要记住！前面两个是父子关系，后面两个是兄弟关系！***

