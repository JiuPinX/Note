## [CSS 背景图片](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML#css_背景图片 "Permalink to CSS 背景图片")

你也可以使用 CSS 把图片嵌入网站中（JavaScript 也行，不过那是另外一个故事了），这个 CSS 属性 [`background-image`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/background-image) 和另其他 `background-*` 属性是用来放置背景图片的。比如，为页面中的所有段落设置一个背景图片，你可以这样做：

```
p {
  background-image: url("images/dinosaur.jpg");
}
```

按理说，这种做法相对于 HTML 中插入图片的做法，可以更好地控制图片和设置图片的位置，那么为什么我们还要使用 HTML 图片呢？如上所述，CSS 背景图片只是为了装饰 — 如果你只是想要在你的页面上添加一些漂亮的东西，来提升视觉效果，那 CSS 的做法是可以的。但是这样插入的图片完全没有语义上的意义，它们不能有任何备选文本，也不能被屏幕阅读器识别。这就是 HTML 图片有用的地方了。

总而言之，如果图像对您的内容里有意义，则应使用 HTML 图像。如果图像纯粹是装饰，则应使用 CSS 背景图片。

**备注：** 你可以在 [CSS](https://developer.mozilla.org/zh-CN/docs/Learn/CSS) 模块里学到更多关于[CSS 背景图片](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Backgrounds_and_borders)的东西。