### [文档片段](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks#文档片段 "Permalink to 文档片段")

超链接除了可以链接到文档外，也可以链接到 HTML 文档的特定部分（被称为**文档片段**）。要做到这一点，你必须首先给要链接到的元素分配一个 [`id`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Global_attributes#id) 属性。例如，如果你想链接到一个特定的标题，可以这样做：

```
<h2 id="Mailing_address">邮寄地址</h2>
```

然后链接到那个特定的 `id`，你可以在 URL 的结尾使用一个井号指向它，例如：

```
<p>要提供意见和建议，请将信件邮寄至<a href="contacts.html#Mailing_address">我们的地址</a>。</p>
```

你甚至可以在同一份文档下，通过链接文档片段，来链接到同一份文档的另一部分：

```
<p>本页面底部可以找到<a href="#Mailing_address">公司邮寄地址</a>。</p>
```