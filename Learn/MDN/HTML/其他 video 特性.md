### [其他 `<video>` 特性](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content#其他_video_特性 "Permalink to 其他 <video> 特性")

这里有许多你可以用在 HTML5 `<video>` 上的特性，请看我们的第三个例子：

```
<video controls width="400" height="400"
       autoplay loop muted
       poster="poster.png">
  <source src="rabbit320.mp4" type="video/mp4">
  <source src="rabbit320.webm" type="video/webm">
  <p>你的浏览器不支持 HTML5 视频。可点击<a href="rabbit320.mp4">此链接</a>观看</p>
</video>
```

这串代码将会给我们呈现出如下页面：

![A video player showing a poster image before it plays. The poster image says HTML5 video example, OMG hell yeah!](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content/poster_screenshot_updated.png)

新的特性：

[`width`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/video#attr-width) 和 [`height`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/video#attr-height)

你可以用属性控制视频的尺寸，也可以用 [CSS](https://developer.mozilla.org/zh-CN/docs/Glossary/CSS) 来控制视频尺寸。无论使用哪种方式，视频都会保持它原始的长宽比 — 也叫做**纵横比**。如果你设置的尺寸没有保持视频原始长宽比，那么视频边框将会拉伸，而未被视频内容填充的部分，将会显示默认的背景颜色。

[`autoplay`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/video#attr-autoplay)

这个属性会使音频和视频内容立即播放，即使页面的其他部分还没有加载完全。建议不要应用这个属性在你的网站上，因为用户们会比较反感自动播放的媒体文件。

[`loop`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/video#attr-loop)

这个属性可以让音频或者视频文件循环播放。同样不建议使用，除非有必要。

[`muted`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/video#attr-muted)

这个属性会导致媒体播放时，默认关闭声音。

[`poster`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/video#attr-poster)

这个属性指向了一个图像的 URL，这个图像会在视频播放前显示。通常用于粗略的预览或者广告。

[`preload`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/video#attr-preload)

这个属性被用来缓冲较大的文件，有 3 个值可选：

-   `"none"` ：不缓冲
-   `"auto"` ：页面加载后缓存媒体文件
-   `"metadata"` ：仅缓冲文件的元数据

你可以点击[这里](https://mdn.github.io/learning-area/html/multimedia-and-embedding/video-and-audio-content/extra-video-features.html)查看以上的例子，也可以点击[这里](https://github.com/mdn/learning-area/blob/gh-pages/html/multimedia-and-embedding/video-and-audio-content/extra-video-features.html)查看源代码。注意我们并没有使用 autoplay 属性在这个版本的例子中 — 如果当页面一加载就开始播放视频的话，就不会看到 poster 属性的效果了。