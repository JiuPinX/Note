## [元数据：<meta> 元素](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#元数据：meta_元素 "Permalink to 元数据：<meta> 元素")

元数据就是描述数据的数据，而 HTML 有一个“官方的”方式来为一个文档添加元数据——[`<meta>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/meta) 元素。当然，其它的在这篇文章中提到的东西也可以被当作元数据。有很多不同种类的 `<meta>` 元素可以被包含进你的页面的 <head> 元素，但是现在我们还不会尝试去解释所有类型，这只会引起混乱。我们会解释一些你常会看到的类型，先让你有个概念。

## [指定你的文档中字符的编码](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#指定你的文档中字符的编码 "Permalink to 指定你的文档中字符的编码")

在上面的示例中，这行是被包含的：

```
<meta charset="utf-8">
```

这个元素简单的指定了文档的字符编码——在这个文档中被允许使用的字符集。`utf-8` 是一个通用的字符集，它包含了任何人类语言中的大部分的字符。意味着该 web 页面可以显示任意的语言；所以对于你的每一个页面都使用这个设置会是一个好主意！比如说，你的页面可以很好的处理英文和日文：

比如说，如果你将你的字符集设置为 `ISO-8859-1`，那么页面将出现乱码：

**备注：** 一些浏览器（比如 Chrome）会自动修正错误的编码，所以取决于你所使用的浏览器，你或许不会看到这个问题。无论如何，你仍然应该为你的页面手动设置编码为 `utf-8`，来避免在其他浏览器中可能出现的潜在问题。

## [添加作者和描述](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#添加作者和描述 "Permalink to 添加作者和描述")

许多 `<meta>` 元素包含了 `name` 和 `content` 属性：

-   `name` 指定了 meta 元素的类型；说明该元素包含了什么类型的信息。
-   `content` 指定了实际的元数据内容。

这两个 meta 元素对于定义你的页面的作者和提供页面的简要描述是很有用的。让我们看一个例子：

```
<meta name="author" content="Chris Mills">
<meta name="description" content="The MDN Web Docs Learning Area aims to provide
complete beginners to the Web with all they need to know to get
started with developing web sites and applications.">
```

指定作者在某些情况下是很有用的：如果你需要联系页面的作者，问一些关于页面内容的问题。一些内容管理系统能够自动获取页面作者的信息，然后用于某些用途。

指定包含关于页面内容的关键字的页面内容的描述是很有用的，因为它可能或让你的页面在搜索引擎的相关的搜索出现得更多（这些行为在术语上被称为：[搜索引擎优化](https://developer.mozilla.org/zh-CN/docs/Glossary/SEO)，或 [SEO](https://developer.mozilla.org/zh-CN/docs/Glossary/SEO)。）

**备注：** 许多 `<meta>` 特性已经不再使用。例如，keyword `<meta>` 元素（`<meta name="keywords" content="fill, in, your, keywords, here">`）——提供关键词给搜索引擎，根据不同的搜索词，查找到相关的网站——已经被搜索引擎忽略了，因为作弊者填充了大量关键词到 keyword，错误地引导搜索结果。

## [其他类型的元数据](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#其他类型的元数据 "Permalink to 其他类型的元数据")

当你在网站上查看源码时，你也会发现其它类型的元数据。你在网站上看到的许多功能都是专有创作，旨在向某些网站（如社交网站）提供可使用的特定信息。

例如，Facebook 编写的元数据协议 [Open Graph Data](https://ogp.me/) 为网站提供了更丰富的元数据。在 MDN Web 文档源代码中，你会发现：

```
<meta property="og:image" content="https://developer.mozilla.org/static/img/opengraph-logo.png">
<meta property="og:description" content="The Mozilla Developer Network (MDN) provides
information about Open Web technologies including HTML, CSS, and APIs for both Web sites
and HTML5 Apps. It also documents Mozilla products, like Firefox OS.">
<meta property="og:title" content="Mozilla Developer Network">
```

上面代码展现的一个效果就是，当你在 Facebook 上链接到 MDN 时，该链接将显示一个图像和描述：这为用户提供更丰富的体验。

![Open graph protocol data from the MDN homepage as displayed on facebook, showing an image, title, and description.](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML/facebook-output.png)

Twitter 还拥有自己的类型的专有元数据协议（称为：[Twitter Cards](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards)），当网站的 URL 显示在 twitter.com 上时，它具有相似的效果。例如下面：

```
<meta name="twitter:title" content="Mozilla Developer Network">
```

## [在你的站点增加自定义图标](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#在你的站点增加自定义图标 "Permalink to 在你的站点增加自定义图标")

为了进一步丰富你的网站设计，你可以在元数据中添加对自定义图标（**favicon**，为“favorites icon”的缩写）的引用，这些将在特定的场合（浏览器的收藏，或书签列表）中显示。

这个不起眼的图标已经存在很多很多年了，16x16 像素是这种图标的第一种类型。你可以看见这些图标出现在浏览器每一个打开的标签页中以及书签页中。

页面添加图标的方式有：

1.  将其保存在与网站的索引页面相同的目录中，以 `.ico` 格式保存（大多数浏览器将支持更通用的格式，如 `.gif` 或 `.png`，但使用 ICO 格式将确保它能在如 Internet Explorer 6 那样古老的浏览器显示）
2.  将以下行添加到 HTML 的 [`<head>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/head) 中以引用它：
    
    ```
    <link rel="icon" href="favicon.ico" type="image/x-icon">
    ```
    

下面是一个 favicon 出现在书签页中的例子：

![The Firefox bookmarks panel, showing a bookmarked example with a favicon displayed next to it.](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML/bookmark-favicon.png)

如今还有很多其他的图标类型可以考虑。例如，你可以在 MDN Web 文档的源代码中找到它：

```
<!-- third-generation iPad with high-resolution Retina display: -->
<link rel="apple-touch-icon-precomposed" sizes="144x144" href="https://developer.mozilla.org/static/img/favicon144.png">
<!-- iPhone with high-resolution Retina display: -->
<link rel="apple-touch-icon-precomposed" sizes="114x114" href="https://developer.mozilla.org/static/img/favicon114.png">
<!-- first- and second-generation iPad: -->
<link rel="apple-touch-icon-precomposed" sizes="72x72" href="https://developer.mozilla.org/static/img/favicon72.png">
<!-- non-Retina iPhone, iPod Touch, and Android 2.1+ devices: -->
<link rel="apple-touch-icon-precomposed" href="https://developer.mozilla.org/static/img/favicon57.png">
<!-- basic favicon -->
<link rel="icon" href="https://developer.mozilla.org/static/img/favicon32.png">
```

这些注释解释了每个图标的用途——这些元素涵盖的东西提供一个高分辨率图标，这些高分辨率图标当网站保存到 iPad 的主屏幕时使用。

不用担心现在实现所有这些类型的图标——这是一个相当先进的功能，你将不会被要求在这个课堂上学习这个知识点。这里的主要目的是让你提前了解有这一样东西以防当你浏览其他网站的源代码时不理解源代码的含义。

**备注：** 如果你的网站使用了内容安全策略（Content Security Policy，CSP）来增加安全性，这个策略会应用在图标上。如果你遇到了图标没有被加载的问题，你需要确认 [`Content-Security-Policy`](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Content-Security-Policy) 响应头的 [img-src 指令 (en-US)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/img-src "Currently only available in English (US)") 没有禁止访问图标。

## [在 HTML 中应用 CSS 和 JavaScript](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#在_html_中应用_css_和_javascript "Permalink to 在 HTML 中应用 CSS 和 JavaScript")

如今，几乎你使用的所有网站都会使用 [CSS](https://developer.mozilla.org/zh-CN/docs/Glossary/CSS) 来让网页更加炫酷，并使用 [JavaScript](https://developer.mozilla.org/zh-CN/docs/Glossary/JavaScript) 来让网页有交互功能，比如视频播放器、地图、游戏以及更多功能。这些应用在网页中很常见，它们分别使用 [`<link>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/link) 元素以及 [`<script>`]`(https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/script) 元素。

-   [`<link>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/link) 元素经常位于文档的头部。这个 link 元素有 2 个属性，`rel="stylesheet"` 表明这是文档的样式表，而 `href` 包含了样式表文件的路径：
    
    ```
    <link rel="stylesheet" href="my-css-file.css">
    ```
    

-   [`<script>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/script) 元素没必要非要放在文档的 `<head>` 中，并包含 `src` 属性来指向需要加载的 JavaScript 文件路径，同时最好加上 `defer` 以告诉浏览器在解析完成 HTML 后再加载 JavaScript。这样可以确保在加载脚本之前浏览器已经解析了所有的 HTML 内容（如果脚本尝试访问某个不存在的元素，浏览器会报错）。实际上还有很多方法可用于处理加载 JavaScript 的问题，但这是现代浏览器中最可靠的一种方法。
    
    ```
    <script src="my-js-file.js" defer></script>
    ```
    

**备注：** `<script>` 元素看起来像一个空元素，但它并不是，因此需要一个结束标记。您还可以选择将脚本放入 `<script>`元素中，而不是指向外部脚本文件。

## [为文档设定主语言](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#为文档设定主语言 "Permalink to 为文档设定主语言")

最后，值得一提的是可以（而且有必要）为站点设定语言，这个可以通过添加 [`lang` 属性](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Global_attributes/lang)到 HTML 开始的标签中来实现（参考 [meta-example.html](https://github.com/mdn/learning-area/blob/main/html/introduction-to-html/the-html-head/meta-example.html)），如下所示：

```
<html lang="zh-CN">
```

这在很多方面都很有用。如果你的 HTML 文档的语言设置好了，那么你的 HTML 文档就会被搜索引擎更有效地索引（例如，允许它在特定于语言的结果中正确显示），对于那些使用屏幕阅读器的视障人士也很有用（例如，法语和英语中都有“six”这个单词，但是发音却完全不同）。

你还可以将文档的分段设置为不同的语言。例如，我们可以把日语部分设置为日语，如下所示：

```
<p>Japanese example: <span lang="ja">ご飯が熱い。</span>.</p>
```

这些代码是根据 [ISO 639-1](https://zh.wikipedia.org/wiki/ISO_639-1) 标准定义的。你可以在 [Language tags in HTML and XML](https://www.w3.org/International/articles/language-tags/) 找到更多相关内容。