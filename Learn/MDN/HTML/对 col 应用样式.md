### [对 `<col>` 应用样式](https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Tables/Basics#对_col_应用样式 "Permalink to 对 <col> 应用样式")

每行都有 `<tr>`，这样方便应用样式，那我们 列 怎么办呢？

```
<table>
  <colgroup>
    <col>
    <col style="background-color: yellow">
  </colgroup>
  <tr>
    <th>Data 1</th>
    <th>Data 2</th>
  </tr>
  <tr>
    <td>Calcutta</td>
    <td>Orange</td>
  </tr>
  <tr>
    <td>Robots</td>
    <td>Jazz</td>
  </tr>
</table>
```

我们使用了两个 `<col>` 来定义“列的样式”，每一个 `<col>` 都会指定每列的样式，对于第一列，我们没有采取任何样式，但是我们仍然需要添加一个空的 `<col>` 元素，如果不这样做，那么我们的样式就会应用到第一列上，这和我们预想的不一样。

如果你想把这种样式信息应用到每一列，我们可以只使用一个 `<col>` 元素，不过需要包含 span 属性，像这样：

```
<colgroup>
  <col style="background-color: yellow" span="2">
</colgroup>
```

就像 `colspan` 和 `rowspan` 一样，`span` 需要一个无单位的数字值，用来指定让这个样式应用到表格中多少列。