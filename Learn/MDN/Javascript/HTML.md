## [块级元素和内联元素](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/Getting_started#块级元素和内联元素 "Permalink to 块级元素和内联元素")

在 HTML 中有两种你需要知道的重要元素类别，块级元素和内联元素。

-   块级元素在页面中以块的形式展现 —— 相对于其前面的内容它会出现在新的一行，其后的内容也会被挤到下一行展现。块级元素通常用于展示页面上结构化的内容，例如段落、列表、导航菜单、页脚等等。一个以 block 形式展现的块级元素不会被嵌套进内联元素中，但可以嵌套在其它块级元素中。
-   内联元素通常出现在块级元素中并环绕文档内容的一小部分，而不是一整个段落或者一组内容。内联元素不会导致文本换行：它通常出现在一堆文字之间，例如超链接元素 [`<a>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/a) 或者强调元素：[`<em>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/em) 和 [`<strong>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/strong)。

看一看下面的例子：

```
<em>第一</em><em>第二</em><em>第三</em>

<p>第四</p><p>第五</p><p>第六</p>
```

[`<em>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/em) 是一个内联元素，所以就像你在下方可以看到的，第一行代码中的三个元素都没有间隙的展示在了同一行。而 [`<p>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/p) 是一个块级元素，所以第二行代码中的每个元素分别都另起了新的一行展现，并且每个段落间都有一些间隔（这是因为默认的浏览器有着默认的展示 [`<p>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/p) 元素的 [CSS 样式](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/First_steps)）。

**备注：** 在这篇文章中提到的“块”和“内联”，不应该与 [CSS 盒子的类型](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/The_box_model#%E5%9D%97%E7%BA%A7%E7%9B%92%E5%AD%90%EF%BC%88block_box%EF%BC%89_%E5%92%8C_%E5%86%85%E8%81%94%E7%9B%92%E5%AD%90%EF%BC%88inline_box%EF%BC%89)中的同名术语相混淆。尽管它们默认是相关的，但改变 CSS 显示类型并不会改变元素的分类，也不会影响它可以包含和被包含于哪些元素。防止这种混淆也是 HTML5 摒弃这些术语的原因之一。

## [布尔属性](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/Getting_started#布尔属性 "Permalink to 布尔属性")

有时你会看到没有值的属性，它是合法的。这些属性被称为布尔属性，他们只能有跟它的属性名一样的属性值。例如[`disabled`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/Input#attr-disabled) 属性，他们可以标记表单输入使之变为不可用 (变灰色)，此时用户不能向他们输入任何数据。

```
<input type="text" disabled="disabled">
```

方便起见，我们完全可以将其写成以下形式（我们还提供了一个非禁止输入的表单元素供你参考，以作为对比）：

```
<!-- 使用 disabled 属性来防止终端用户输入文本到输入框中 -->
<input type="text" disabled>

<!-- 下面这个输入框没有 disabled 属性，所以用户可以向其中输入 -->
<input type="text">
```

## [单引号或者双引号？](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/Getting_started#单引号或者双引号？ "Permalink to 单引号或者双引号？")

在目前为止，本章内容所有的属性都是由双引号来包裹。也许在一些 HTML 中，你以前也见过单引号。这只是风格的问题，你可以从中选择一个你喜欢的。以下两种情况都可以：

```
<a href="http://www.example.com">示例站点链接</a>

<a href='http://www.example.com'>示例站点链接</a>
```

但你应该注意单引号和双引号不能在一个属性值里面混用。下面的语法是错误的：

```
<a href="http://www.example.com'>示例站点链接</a>
```

在一个 HTML 中已使用一种引号，你可以在此引号中嵌套另外一种引号：

```
<a href="http://www.example.com" title="你觉得'好玩吗'？">示例站点链接</a>
```

如果你想将引号当作文本显示在 html 中，你就必须使用[实体引用](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/Getting_started#%E5%AE%9E%E4%BD%93%E5%BC%95%E7%94%A8%EF%BC%9A%E5%9C%A8_html_%E4%B8%AD%E5%8C%85%E5%90%AB%E7%89%B9%E6%AE%8A%E5%AD%97%E7%AC%A6)。

## [HTML 注释](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/Getting_started#html_注释 "Permalink to HTML 注释")

如同大部分的编程语言一样，在 HTML 中有一种可用的机制来在代码中书写注释 —— 注释是被浏览器忽略的，而且是对用户不可见的，它们的目的是允许你描述你的代码是如何工作的和不同部分的代码做了什么等等。如果你在半年后重新返回你的代码库，而且不能记起你所做的事情 —— 或者当你处理别人的代码的时候，那么注释是很有用的。

为了将一段 HTML 中的内容置为注释，你需要将其用特殊的记号<!--和-->包括起来，比如：

```
<p>我在注释外！</p>

<!-- <p>我在注释内！</p> -->
```

正如你下面所见的那样，第一段出现在了实时输出中，但是第二段却没有。