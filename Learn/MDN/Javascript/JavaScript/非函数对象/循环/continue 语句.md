## [`continue` 语句](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Loops_and_iteration#continue_语句)

[`continue`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Statements/continue) 语句可以用来继续执行（跳过代码块的剩余部分并进入下一循环）一个 `while`、`do-while`、`for`，或者 `label` 语句。

-   当你使用不带 label 的 `continue` 时，它终止当前 `while`，`do-while`，或者 for 语句到结尾的这次的循环并且继续执行下一次循环。
-   当你使用带 label 的 `continue` 时，它会应用被 label 标识的循环语句。

`continue` 语句的语法看起来像这样：

```
continue [label];
```

### [**例子 1**](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Loops_and_iteration#例子_1_3)

The following example shows a `while` loop with a `continue` statement that executes when the value of `i` is three. Thus, `n` takes on the values one, three, seven, and twelve.

```
var i = 0;
var n = 0;
while (i < 5) {
  i++;
  if (i == 3) {
    continue;
  }
  n += i;
  console.log(n);
}
//1,3,7,12
```

```
var i = 0;
var n = 0;
while (i < 5) {
  i++;
  if (i == 3) {
     // continue;
  }
  n += i;
  console.log(n);
}
// 1,3,6,10,15
```

### [**例子 2**](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Loops_and_iteration#例子_2_3)

一个被标签为 `checkiandj` 的语句包含了一个标签为 `checkj` 的语句。

如果遇到 `continue` 语句，程序会结束当前 `chechj` 的迭代并开始下一轮的迭代。

每次遇到 `continue` 语句时，`checkj` 语句会一直重复执行，直到 `checkj` 语句的条件为 `false`。

当返回 `false` 后，将会执行 `checkiandj` 的剩余语句，`checkiandj` 会一直执行，直到 `checkiandj` 的条件为 `false`。

当 `checkiandj` 的返回值为 `false` 时，将会执行 `checkiandj` 的下面的语句。

如果 `continue` 有一个标记 `checkiandj`，程序将会从 `checkiandj` 语句块的顶部继续执行。

```
var i = 0;
var j = 10;
checkiandj:
  while (i < 4) {
    console.log(i);
    i += 1;
    checkj:
      while (j > 4) {
        console.log(j);
        j -= 1;
        if ((j % 2) == 0) {
          continue checkj;
        }
        console.log(j + ' 是奇数。');
      }
      console.log('i = ' + i);
      console.log('j = ' + j);
  }
```