## [`do...while` 语句](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Loops_and_iteration#do...while_语句)

[`do...while`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Statements/do...while) 语句一直重复直到指定的条件求值得到假值（false）。一个 do...while 语句看起来像这样：

do
  statement
while (condition);

`statement` 在检查条件之前会执行一次。要执行多条语句（语句块），要使用块语句（`{ ... }`）包括起来。如果 `condition` 为真（true），`statement` 将再次执行。在每个执行的结尾会进行条件的检查。当 `condition` 为假（false），执行会停止并且把控制权交回给 `do...while` 后面的语句。

### [**例子**](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Loops_and_iteration#例子_2)

在下面的例子中，这个 `do` 循环将至少重复一次，并且一直重复直到 `i` 不再小于 5。

```
var i = 0;
do {
  i += 1;
  console.log(i);
} while (i < 5);
```