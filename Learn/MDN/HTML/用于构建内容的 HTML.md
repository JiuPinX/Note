## [用于构建内容的 HTML](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure#用于构建内容的_html "Permalink to 用于构建内容的 HTML")

以上简单示例不是很精美，但是足够说明网站的典型布局方式了。一些站点拥有更多列，其中一些远比这复杂，但一切在你掌握之中。通过合适的 CSS，你可以使用相当多种的任意页面元素来环绕在不同的页面区域来做成你想要的样子，但如前所述，我们要敬畏语义，做到**正确选用元素**。

这是因为视觉效果并不是一切。我们可以修改最重要内容（例如导航菜单和相关链接）的颜色、字体大小来吸引用户的注意，但是这对视障人士是无效的，“粉红色”和“大字体”对他们并不奏效。

**备注：** [全球色盲患者比例为 4%](http://www.color-blindness.com/2006/04/28/colorblind-population/)，换句话说，每 12 名男性就有一位色盲，每 200 名女性就有一位色盲。全盲和视障人士约占世界人口（[约 70 亿](https://en.wikipedia.org/wiki/World_human_population#/media/File:World_population_history.svg)）的 13％（2015 年 [全球约有 9.4 亿人口存在视力问题](https://en.wikipedia.org/wiki/Visual_impairment)）。

HTML 代码中可根据功能来为区段添加标记。可使用元素来无歧义地表示上文所讲的内容区段，屏幕阅读器等辅助技术可以识别这些元素，并帮助执行“找到主导航“或”找到主内容“等任务。参见前文所讲的 [页面中元素结构和语义不佳所带来的后果](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/HTML_text_fundamentals#%e4%b8%ba%e4%bb%80%e4%b9%88%e6%88%91%e4%bb%ac%e9%9c%80%e8%a6%81%e7%bb%93%e6%9e%84%e5%8c%96)。

为了实现语义化标记，HTML 提供了明确这些区段的专用标签，例如：

-   [`<header>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/header)：页眉。
-   [`<nav>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/nav)：导航栏。
-   [`<main>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/main)：主内容。主内容中还可以有各种子内容区段，可用[`<article>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/article)、[`<section>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/section) 和 [`<div>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/div) 等元素表示。
-   [`<aside>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/aside)：侧边栏，经常嵌套在 [`<main>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/main) 中。
-   [`<footer>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/footer)：页脚。

### [主动学习：研究示例代码](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure#主动学习：研究示例代码 "Permalink to 主动学习：研究示例代码")

上图的示例可用下面的代码表示（完整代码请参见 [GitHub](https://github.com/roy-tian/learning-area/blob/master/html/introduction-to-html/document-and-website-structure/index.html)），请结合图片观察代码，并找出代码中可见的区段：

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>二次元俱乐部</title>
    <link href="https://fonts.googleapis.com/css?family=Open+Sans+Condensed:300|Sonsie+One" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css?family=ZCOOL+KuaiLe" rel="stylesheet">
    <link href="style.css" rel="stylesheet">
  </head>

  <body>
    <header> <!-- 本站所有网页的统一主标题 -->
      <h1>聆听电子天籁之音</h1>
    </header>

    <nav> <!-- 本站统一的导航栏 -->
      <ul>
        <li><a href="#">主页</a></li>
        <!-- 共 n 个导航栏项目，省略…… -->
      </ul>

      <form> <!-- 搜索栏是站点内导航的一个非线性的方式。 -->
        <input type="search" name="q" placeholder="要搜索的内容">
        <input type="submit" value="搜索">
      </form>
    </nav>

    <main> <!-- 网页主体内容 -->
      <article>
        <!-- 此处包含一个 article（一篇文章），内容略…… -->
      </article>

      <aside> <!-- 侧边栏在主内容右侧 -->
        <h2>相关链接</h2>
        <ul>
          <li><a href="#">这是一个超链接</a></li>
          <!-- 侧边栏有 n 个超链接，略略略…… -->
        </ul>
      </aside>
    </main>

    <footer> <!-- 本站所有网页的统一页脚 -->
      <p>© 2050 某某保留所有权利</p>
    </footer>
  </body>
</html>
```

请花一些时间来阅读，其中的注释应该能够帮助你理解这些代码。现在能够理解上面的代码就可以，因为编写一套正确的 HTML 结构是理解文档布局的前提，布局工作就交给 CSS 吧。在学习 CSS 一章时我们再展开介绍。