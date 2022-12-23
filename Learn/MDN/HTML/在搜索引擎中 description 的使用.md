### [实践操作：在搜索引擎中 description 的使用](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML#实践操作：在搜索引擎中_description_的使用 "Permalink to 实践操作：在搜索引擎中 description 的使用")

description 也被使用在搜索引擎显示的结果页中。下面通过一个例子来说明：

1.  访问 [MDN Web 文档](https://developer.mozilla.org/zh-CN/)。
2.  查看网页源代码（通过鼠标右键点击网页在弹出的菜单中选择_查看网页源代码_）
3.  找到 description 的 meta 标签。就和如下展示的这样：
    
    ```
    <meta name="description" content="The MDN Web Docs site
      provides information about Open Web technologies
      including HTML, CSS, and APIs for both Web sites and
      progressive web apps.">
    ```
    

2.  现在，在你喜欢的搜索引擎里搜索“MDN Web Docs”（下图展示的是在谷歌搜索里的情况）。你会看到 description `<meta>` 和 `<title>` 元素如何在搜索结果里显示——很值得这样做哦！ ![A Yahoo search result for "Mozilla Developer Network"](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML/mdn-search-result.png)

**备注：** 在谷歌搜索里，在主页面链接下面，你将看到一些相关子页面——这些是站点链接，可以在 [Google's webmaster tools](https://search.google.com/search-console/about) 配置——一种可以使你的站点对搜索引擎更友好的方式。

**备注：** 许多 `<meta>` 特性已经不再使用。例如，keyword `<meta>` 元素（`<meta name="keywords" content="fill, in, your, keywords, here">`）——提供关键词给搜索引擎，根据不同的搜索词，查找到相关的网站——已经被搜索引擎忽略了，因为作弊者填充了大量关键词到 keyword，错误地引导搜索结果。