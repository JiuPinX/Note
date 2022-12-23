## [`<audio>` 标签](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content#audio_%E6%A0%87%E7%AD%BE)

[`<audio>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/audio) 标签与 [`<video>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/video) 标签的使用方式几乎完全相同，有一些细微的差别比如下面的边框不同，一个典型的例子如下：

[`<audio>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/audio) 标签与 [`<video>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/video) 标签的使用方式几乎完全相同，有一些细微的差别比如下面的边框不同，一个典型的例子如下：

```
<audio controls>
  <source src="viper.mp3" type="audio/mp3">
  <source src="viper.ogg" type="audio/ogg">
  <p>你的浏览器不支持 HTML5 音频，可点击<a href="viper.mp3">此链接</a>收听。</p>
</audio>
```

这串代码将会产生如下的效果：

![A simple audio player with a play button, timer, volume control, and progress bar](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content/audio-player.png)

**备注：** 你可以点击这里[查看](https://mdn.github.io/learning-area/html/multimedia-and-embedding/video-and-audio-content/multiple-audio-formats.html)以上例子，或者点击[这里](https://github.com/mdn/learning-area/blob/gh-pages/html/multimedia-and-embedding/video-and-audio-content/multiple-audio-formats.html)查看源代码。

音频播放器所占用的空间比视频播放器要小，由于它没有视觉部件 — 你只需要显示出能控制音频播放的控件。一些与 HTML5 `<video>` 的差异如下：

-   [`<audio>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/audio) 标签不支持 `width`/`height` 属性 — 由于其并没有视觉部件，也就没有可以设置 `width`/`height` 的内容。
-   同时也不支持 `poster` 属性 — 同样，没有视觉部件。

除此之外，`<audio>` 标签支持所有 `<video>` 标签拥有的特性 — 你可以回顾上面的章节来了解更多的有关信息。