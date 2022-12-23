### [在下载链接时使用 download 属性](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks#在下载链接时使用_download_属性 "Permalink to 在下载链接时使用 download 属性")

当你链接到要下载的资源而不是在浏览器中打开时，你可以使用 download 属性来提供一个默认的保存文件名。下面是一个 Firefox 的 Windows 最新版本下载链接的示例：

```
<a href="https://download.mozilla.org/?product=firefox-latest-ssl&os=win64&lang=zh-CN"
   download="firefox-latest-64bit-installer.exe">
  下载最新的 Firefox 中文版 - Windows（64 位）
</a>
```