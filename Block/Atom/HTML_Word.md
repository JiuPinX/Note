HTML Word 是 HTML 的一个模块

## 示例

### 结构化

#### 标题

```
<h1>我是一级标题</h1>
<h2>我是二级标题</h2>
<h3>我是三级标题</h3>
<h4>我是四级标题</h4>
<h5>我是五级标题</h5>
<h6>我是六级标题</h6>
```

#### 段落

```
<p>大家好！</p>
<p>我是一个段落！</p>
```

#### 块引用

```
<blockquote cite="https://developer.mozilla.org/en-US/">
    <p>Documenting web technologies, including CSS, HTML, and JavaScript, since 2005.</p>
</blockquote>
```

#### 插入文档

```
<ins cite="../howtobeawizard.html" datetime="2018-05">
    <ins>这一段文本是新插入至文档的。</ins>
</ins>
```

#### 标记联系方式

```
<address>
    <p>页面编写者<a href="联系方式链接">九品</a></p>
</address>
```

### 格式化

#### 标记

```
<b>粗体文字</b>
<strong>这段文字很重要</strong>

<i>斜体文本</i>
<em>这段文字被强调</em>

<u>下划线文本</u>
<ins>这一段文本是新插入至文档的。</ins>

<del>删除的文本</del>

<mark>被标记的文本</mark>

<q>引用的文本，浏览器在引用的周围插入了引号</q>
<q cite="http://en.wikipedia.org/wiki/Kenny_McCormick#Cultural_impact">
Oh my God, you/they killed Kenny!
</q>
```

#### 排版

```
<bdi>使文本双向隔离</bdi>

<sup>使文本上标</sup>
<sub>使文本下标</sub>

<small>使文本变小</small>

<ruby>
  汉 <rp>(</rp><rt>han</rt><rp>)</rp>
  字 <rp>(</rp><rt>zi</rt><rp>)</rp>
</ruby>

<ruby>
  明 日 <rp>(</rp><rt>ming ri</rt><rp>)</rp>
</ruby>

<abbr title="超文本标记语言（Hyper text Markup Language）">HTML</abbr>
```

#### 计算机

```
<code>代码</code>

<pre>预格式化文本</pre>

<var>具体变量名</var>

<kbd>用户输入</kbd>

<samp>计算机程序的输出<samp>

<time datetime="2016-01-20">2016 年 1 月 20 日</time>
```

**备注：**

这里是最好的经验法则：如果没有更合适的元素，那么使用 `<b>`、`<i>` 或 `<u>` 来表达传统上的粗体、斜体或下划线表达的意思是合适的。然而，始终拥有无障碍的思维模式是至关重要的。斜体的概念对人们使用屏幕阅读器是没有帮助的，对使用其他书写系统而不是拉丁文书写系统的人们也是没有帮助的。

- `<i>` 被用来传达传统上用斜体表达的意义：外国文字，分类名称，技术术语，一种思想……
- `<b>` 被用来传达传统上用粗体表达的意义：关键字，产品名称，引导句……
- `<u>` 被用来传达传统上用下划线表达的意义：专有名词，拼写错误……

## 参考

### HTML 元素

#### 结构

- [`<h1>`-`<h6>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/Heading_Elements)

- [`<p>`]()

- [`<blockquote>`]()

- [`<ins>`]()

- [`<address>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/address)

#### 格式

##### 标记

- [`<b>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/b)

- [`<strong>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/strong)

- [`<i>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/i)

- [`<em>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/em)

- [`<u>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/u)

- [`<ins>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/ins)

- [`<mark>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/mark)

- [`<q>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/q)

##### 排版

- [`<bdi>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/bdi)

- [`<sup>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/sup)

- [`<sub>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/sub)

- [`<small>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/small)

- [`<ruby>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/ruby)

- [`<rp>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/rp)

- [`<rt>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/rt)

- [`<abbr>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/abbr)

##### 计算机

- [`<code>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/code)

- [`<pre>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/pre)

- [`<var>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/var)

- [`<kbd>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/kbd)

- [`<samp>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/samp)

- [`<time>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/time)
