## [在 HTML 中应用 CSS 和 JavaScript](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#在_html_中应用_css_和_javascript "Permalink to 在 HTML 中应用 CSS 和 JavaScript")

如今，几乎你使用的所有网站都会使用 [CSS](https://developer.mozilla.org/zh-CN/docs/Glossary/CSS) 来让网页更加炫酷，并使用 [JavaScript](https://developer.mozilla.org/zh-CN/docs/Glossary/JavaScript) 来让网页有交互功能，比如视频播放器、地图、游戏以及更多功能。这些应用在网页中很常见，它们分别使用 [`<link>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/link) 元素以及[`<s script>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/script) 元素。

-   [`<link>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/link) 元素经常位于文档的头部。这个 link 元素有 2 个属性，`rel="stylesheet"` 表明这是文档的样式表，而 `href` 包含了样式表文件的路径：
    
    ```
    <link rel="stylesheet" href="my-css-file.css">
    ```
    

-   [`<s script>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/script) 元素没必要非要放在文档的 `<head>` 中，并包含 `src` 属性来指向需要加载的 JavaScript 文件路径，同时最好加上 `defer` 以告诉浏览器在解析完成 HTML 后再加载 JavaScript。这样可以确保在加载脚本之前浏览器已经解析了所有的 HTML 内容（如果脚本尝试访问某个不存在的元素，浏览器会报错）。实际上还有很多方法可用于处理加载 JavaScript 的问题，但这是现代浏览器中最可靠的一种方法。
    
    ```
    <script src="my-js-file.js" defer></script>
    ```
    

**备注：** `<s script>` 元素看起来像一个空元素，但它并不是，因此需要一个结束标记。您还可以选择将脚本放入 `<s script>`元素中，而不是指向外部脚本文件。