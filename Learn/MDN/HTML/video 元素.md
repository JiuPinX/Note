## [`<video>` 元素](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content#video_元素 "Permalink to <video> 元素")

[`<video>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/video) 允许你轻松地嵌入一段视频。一个简单的例子如下：

```
<video src="rabbit320.webm" controls>
  <p>你的浏览器不支持 HTML5 视频。可点击<a href="rabbit320.mp4">此链接</a>观看</p>
</video>
```

当中的一些属性如下：

[`src`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/video#attr-src)

同 [`<img>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/img) 标签使用方式相同，`src` 属性指向你想要嵌入网页当中的视频资源，他们的使用方式完全相同。

[`controls`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/video#attr-controls)

用户必须能够控制视频和音频的回放功能。你可以使用 `controls` 来包含浏览器提供的控件界面，同时你也可以使用合适的 [JavaScript API](https://developer.mozilla.org/zh-CN/docs/Web/API/HTMLMediaElement) 创建自己的界面。界面中至少要包含开始、停止以及调整音量的功能。

`<video>` 标签内的内容

这个叫做**后备内容** — 当浏览器不支持 `<video>` 标签的时候，就会显示这段内容，这使得我们能够对旧的浏览器提供回退内容。你可以添加任何后备内容，在这个例子中我们提供了一个指向这个视频文件的链接，从而使用户至少可以访问到这个文件，而不会局限于浏览器的支持。

已嵌入视频文件的网页样式如下：

![A simple video player showing a video of a small white rabbit](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content/simple-video.png)

你可以点击[这里](https://mdn.github.io/learning-area/html/multimedia-and-embedding/video-and-audio-content/simple-video.html)查看网页，或者点击[这里](https://github.com/mdn/learning-area/blob/master/html/multimedia-and-embedding/video-and-audio-content/simple-video.html)查看源代码。