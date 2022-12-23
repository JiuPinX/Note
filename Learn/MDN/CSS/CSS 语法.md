CSS（层叠样式表）用于设置和布置网页——例如，更改内容的字体、颜色、大小和间距，将其拆分为多个列，或添加动画和其他装饰功能。这个模块为你掌握 CSS 的过程提供了一个温和的开端，包括它如何工作的基础知识，语法是什么样的，以及如何开始使用它来为 HTML 添加样式。

*响应式* *布局* 中有被 *选择器* *样式化* 的 *盒模型*



## [CSS 模块](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/First_steps/What_is_CSS#css_模块 "Permalink to CSS 模块")

你可以通过 CSS 为许多东西添加样式，CSS 由许多*模块 (modules)* 构成。你可以在 MDN 上浏览这些模块的参考内容 (MDN reference)，许多模块都被组织在自己单独的文档页面。例如，我想查找一下 MDN reference 的 [Backgrounds and Borders](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_Backgrounds_and_Borders) 模块的相关内容，来了解它是用来做什么的、它还包括什么属性、它还有什么其它特性等。你也可以在 _CSS Specification_ 查找（见下文），它定义了 CSS 规范。

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