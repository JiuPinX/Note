## [`while` 语句](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Loops_and_iteration#while_语句)

一个 [`while`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Statements/while) 语句只要指定的条件求值为真（true）就会一直执行它的语句块。一个 `while` 语句看起来像这样：

while (condition)
  statement

如果这个条件变为假，循环里的 `statement` 将会停止执行并把控制权交回给 `while` 语句后面的代码。

条件检测会在每次 `statement` 执行之前发生。如果条件返回为真， `statement` 会被执行并紧接着再次测试条件。如果条件返回为假，执行将停止并把控制权交回给 while 后面的语句。

要执行多条语句（语句块），要使用语句块 (`{ ... }`) 包括起来。

### [**例子 1**](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Loops_and_iteration#例子_1)

只要 `n` 小于 3，下面的 `while` 循环就会一直执行：

```
var n = 0;
var x = 0;
while (n < 3) {
  n++;
  x += n;
}
```

在每次循环里， `n` 会增加 1，并被加到 `x` 上。所以，x 和 n 的变化是：

-   第一次完成后：`n` = 1，`x` = 1
-   第二次完成后：`n` = 2，`x` = 3
-   第三次完成后：`n` = 3，`x` = 6

在三次完成后，条件 `n < 3` 的结果不再为真，所以循环终止了。

### [**例子 2**](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Loops_and_iteration#例子_2_2)

避免无穷循环（无限循环）。保证循环的条件结果最终会变成假；否则，循环永远不会停止。因为条件永远不会变成假值，下面这个 while 循环将会永远执行：

```
while (true) {
  console.log("Hello, world");
}
```