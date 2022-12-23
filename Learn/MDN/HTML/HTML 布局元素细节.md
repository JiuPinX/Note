## [HTML 布局元素细节](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure#html_布局元素细节 "Permalink to HTML 布局元素细节")

理解所有 HTML 区段元素具体含义是很有益处的，这一点将随着个人 web 开发经验的逐渐丰富日趋显现。更多细节请查阅 [HTML 元素参考](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element)。现在，你只需要理解以下主要元素的意义：

-   [`<main>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/main) 存放每个页面独有的内容。每个页面上只能用一次 `<main>`，且直接位于 [`<body>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/body) 中。最好不要把它嵌套进其它元素。
-   [`<article>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/article) 包围的内容即一篇文章，与页面其它部分无关（比如一篇博文）。
-   [`<section>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/section) 与 `<article>` 类似，但 `<section>` 更适用于组织页面使其按功能（比如迷你地图、一组文章标题和摘要）分块。一般的最佳用法是：以 [标题](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Howto/Set_up_a_proper_title_hierarchy) 作为开头；也可以把一篇 `<article>` 分成若干部分并分别置于不同的 `<section>` 中，也可以把一个区段 `<section>` 分成若干部分并分别置于不同的 `<article>` 中，取决于上下文。
-   [`<aside>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/aside) 包含一些间接信息（术语条目、作者简介、相关链接，等等）。
-   [`<header>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/header) 是简介形式的内容。如果它是 [`<body>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/body) 的子元素，那么就是网站的全局页眉。如果它是 [`<article>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/article) 或[`<section>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/section) 的子元素，那么它是这些部分特有的页眉（此 `<header>` 非彼 [标题](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#%e5%a2%9e%e5%8a%a0%e4%b8%80%e4%b8%aa%e6%a0%87%e9%a2%98)）。
-   [`<nav>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/nav) 包含页面主导航功能。其中不应包含二级链接等内容。
-   [`<footer>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/footer) 包含了页面的页脚部分。