HTML Table 是 HTML 的一个模块

## 示例

### 常规

```
<table>
    <tr>
        <td></td>
        <th>富士康</th>
        <th>大渡口</th>
    </tr>
    <tr>
        <th>城市</th>
        <td>郑州</td>
        <td>重庆</td>
    </tr>
    <tr>
        <th>时间</th>
        <td>11月23日</td>
        <td>1月7日</td>
    </tr>
    <tr>
        <th>性质</th>
        <td colspan="2">工人运动</td>
    </tr>
</table>
```

### 复杂

```
<table>
    <caption>Title</caption>
    <colgroup>...</colgroup>
    <thead>...</thead>
    <tbody>...</tbody>
    <tfoot>...</tfoot>
</table>

```

### `scope`

```
<tr>
    <td></td>
    <th scope="colgroup" colspan="4">列列标题</th>
</tr>
<tr>
    <td></td>
    <th scope="col">列标题</th>
    <th scope="col">列标题</th>
    <th scope="col">列标题</th>
    <th scope="col">列标题</th>
</tr>
<tr>
    <th scope="row">行标题</th>
    <td>苹果</td>
    <td>土豆</td>
    <td>迫击炮</td>
    <td>豌豆</td>
</tr>
```

### `id`

```
<thead>
  <tr>
    <th id="purchase">Purchase</th>
    <th id="location">Location</th>
    <th id="date">Date</th>
    <th id="evaluation">Evaluation</th>
    <th id="cost">Cost (€)</th>
  </tr>
</thead>
<tbody>
<tr>
  <th id="haircut">Haircut</th>
  <td headers="location haircut">Hairdresser</td>
  <td headers="date haircut">12/09</td>
  <td headers="evaluation haircut">Great idea</td>
  <td headers="cost haircut">30</td>
</tr>

  ...

</tbody>

```

### `<colgroup>`

```
<colgroup>
    <col span="2">
    <col>
</colgroup>
```

## 参考

### HTML 元素

#### 基础

- [`<table>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/table)

- [`<tr>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/tr)

- [`<th>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/th)

#### 进阶

- [`<thead>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/thead)

- [`<tbody>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/tbody)

- [`<tfoot>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/tfoot)

#### 其他

- [`<caption>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/caption)

- [`<colgroup>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/colgroup)

- [`<col>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/col)

### 指南

- [HTML 表格](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Tables)

- [HTML 表格基础](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Tables/Basics)

- [HTML 表格高级功能与无障碍](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Tables/Advanced)
