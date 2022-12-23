## 使用例

[[HTML特定片段链接]]

[[在下载链接时使用 download 属性]]

[[电子邮件链接]]

## [统一资源定位符（URL）与路径（path）快速入门](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks#统一资源定位符（url）与路径（path）快速入门 "Permalink to 统一资源定位符（URL）与路径（path）快速入门")

要全面地了解链接目标，你需要了解统一资源定位符和文件路径。本小节将介绍相关的信息。

统一资源定位符（英文：**U**niform **R**esource **L**ocator，简写：URL）是一个定义了在网络上的位置的一个文本字符串。例如 Mozilla 的中文主页定位在 `https://www.mozilla.org/zh-CN/`.

URL 使用路径查找文件。路径指定文件系统中你感兴趣的文件所在的位置。看一下一个简单的目录结构的例子（参见[创建超链接](https://github.com/mdn/learning-area/tree/main/html/introduction-to-html/creating-hyperlinks)目录。）

![A simple directory structure. The parent directory is called creating-hyperlinks and contains two files called index.html and contacts.html, and two directories called projects and pdfs, which contain an index.html and a project-brief.pdf file, respectively](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks/simple-directory.png)

此目录结构的**根目录**称为 `creating-hyperlinks`。当在网站上工作时，你会有一个包含整个网站的目录。在根目录，我们有一个 `index.html` 和一个 `contacts.html` 文件。在真实的网站上，`index.html` 将会成为我们的主页或登录页面（作为网站或网站特定部分的入口的网页。）。

我们的根目录还有两个目录——`pdfs` 和 `projects`，它们分别包含一个 PDF（`project-brief.pdf`）文件和一个 `index.html` 文件。请注意你可以有两个 `index.html` 文件，前提是他们在不同的目录下，许多网站就是如此。第二个 `index.html` 或许是项目相关信息的主登录界面。

-   **指向当前目录**：如果 `index.html`（目录顶层的 `index.html`）想要包含一个超链接指向 `contacts.html`，你只需要指定想要链接的文件名，因为它与当前文件是在同一个目录的。所以你应该使用的 URL 是 `contacts.html`:
    
    ```
    <p>要联系某位工作人员，请访问我们的<a
     href="contacts.html">联系人页面</a>。</p>
    ```
    

-   **指向子目录**：如果 `index.html` （目录顶层 `index.html`）想要包含一个超链接指向 `projects/index.html`，你需要先进入 `projects` 项目目录，然后指明要链接到的文件 `index.html`。通过指定目录的名称，然后是正斜杠，然后是文件的名称。因此你要使用的 URL 是 `projects/index.html`：
    
    ```
    <p>请访问<a href="projects/index.html">项目页面</a>。</p>
    ```
    

-   **指向上级目录**：如果你想在 `projects/index.html` 中包含一个指向 `pdfs/project-brief.pdf` 的超链接，你必须先返回上级目录，然后再回到 `pdf` 目录。“返回上一个目录级”使用两个英文点号表示（`..`），所以你应该使用的 URL 是 `../pdfs/project-brief.pdf`：
    
    ```
    <p>点击打开<a href="../pdfs/project-brief.pdf">项目简介</a>。</p>
    ```
    

**备注：** 如果需要的话，你可以将这些功能的多个例子和复杂的 URL 结合起来。例如：`../../../complex/path/to/my/file.html`。