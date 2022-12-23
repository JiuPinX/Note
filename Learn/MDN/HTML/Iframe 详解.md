## [Iframe 详解](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Multimedia_and_embedding/Other_embedding_technologies#iframe_详解 "Permalink to Iframe 详解")

是不是很简单又有趣呢？[`<iframe>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/iframe) 元素旨在允许你将其他 Web 文档嵌入到当前文档中。这很适合将第三方内容嵌入你的网站，你可能无法直接控制，也不希望实现自己的版本——例如来自在线视频提供商的视频，[Disqus](https://disqus.com/) 等评论系统，在线地图提供商，广告横幅等。你通过本课程使用的实时可编辑示例就是使用 `<iframe>` 实现的。

我们会在后面提到，关于 `<iframe>` 有一些严重的[安全隐患](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Multimedia_and_embedding/Other_embedding_technologies#%E5%AE%89%E5%85%A8%E9%9A%90%E6%82%A3)需要考虑，但这并不意味着你不应该在你的网站上使用它们——它只需要一些知识和仔细地思考。让我们更详细地探索这些代码。假设你想在其中一个网页上加入 MDN 词汇表，你可以尝试以下方式：

```
<iframe src="https://developer.mozilla.org/zh-CN/docs/Glossary"
        width="100%" height="500" frameborder="0"
        allowfullscreen sandbox>
  <p> <a href="https://developer.mozilla.org/zh-CN/docs/Glossary">
    Fallback link for browsers that don't support iframes
  </a> </p>
</iframe>
```

此示例包括使用以下所需的 `<iframe>` 基本要素：

[`allowfullscreen`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/iframe#attr-allowfullscreen)

如果设置，`<iframe>`则可以通过[全屏 API](https://developer.mozilla.org/zh-CN/docs/Web/API/Fullscreen_API) 设置为全屏模式（稍微超出本文的范围）。

[`frameborder`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/iframe#attr-frameborder)

如果设置为 1，则会告诉浏览器在此框架和其他框架之间绘制边框，这是默认行为。0 删除边框。不推荐这样设置，因为在 [CSS 中](https://developer.mozilla.org/zh-CN/docs/Glossary/CSS)可以更好地实现相同的效果。[`border`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/border)`: none;`

[`src`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/iframe#attr-src)

该属性与 [`<video>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/video) / 元素表示文档中的图像。[`<img>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/img)一样包含指向要嵌入文档的 URL 路径。

[`width`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/iframe#attr-width) 和 [`height`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/iframe#attr-height)

这些属性指定你想要的 iframe 的宽度和高度。

### 备选内容

与 [`<video>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/video) 等其它类似元素相同，你可以在 `<iframe></iframe>` 标签之间包含备选内容，如果浏览器不支持 `<iframe>`，将会显示备选内容，这种情况下，我们已经添加了一个到该页面的链接。现在你几乎不可能遇到任何不支持 `<iframe>` 的浏览器。

[`sandbox`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/iframe#attr-sandbox)

该属性需要在已经支持其它 `<iframe>` 功能（例如 IE 10 及更高版本）但稍微更现代的浏览器上才能工作，该属性可以提高安全性设置；我们将在下一节中更加详细地谈到。

**备注：** 为了提高速度，在主内容完成加载后，使用 JavaScript 设置 iframe 的 `src` 属性是个好主意。这使你的页面可以更快地被使用，并减少你的官方页面加载时间（重要的 [SEO](https://developer.mozilla.org/zh-CN/docs/Glossary/SEO) 指标）。