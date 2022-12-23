### [`if...else` 语句](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#if...else_语句)

当一个逻辑条件为真，用 if 语句执行一个语句。当这个条件为假，使用可选择的 else 从句来执行这个语句。if 语句如下所示：

```
if (condition) {
  statement_1;
}else {
  statement_2;
} //推荐使用严格的语句块模式，语句 else 可选
```

条件可以是任何返回结果被计算为 true 或 false 的表达式。如果条件表达式返回的是 true，statement_1 语句会被执行；否则，statement_2 被执行。statement_1 和 statement_2 可以是任何语句，甚至你可以将另一个 if 语句嵌套其中。

你也可以组合语句通过使用 `else if` 来测试连续多种条件判断，就像下面一样：

```
if (condition_1) {
  statement_1;
}else if (condition_2) {
  statement_2;
}else if (condition_n_1) {
  statement_n;
}else {
  statement_last;
}
```

要执行多个语句，可以使用语句块 ({ ... }) 来分组这些语句。通常，总是使用语句块是一个好的习惯，特别是在代码涉及比较多的 if 语句时：

```
if (条件) {
  当条件为真的时候，执行语句 1;
  当条件为真的时候，执行语句 2;
} else {
  当条件为假的时候，执行语句 3;
  当条件为假的时候，执行语句 4;
}
```

不建议在条件表达式中使用赋值语句，因为在快速查阅代码时容易把它看成等值比较。例如，不要使用下面的代码：

**警告：**

```
  if(x = y){
    /*  语句  */
  }
```

如果你需要在条件表达式中使用赋值，通常在赋值语句前后额外添加一对括号。例如：

if ((x = y)) {
  /* statements here */
}

#### 错误的值

下面这些值将被计算出 false (also known as [Falsy](https://developer.mozilla.org/zh-CN/docs/Glossary/Falsy) values):

-   `false`
-   `undefined`
-   `null`
-   `0`
-   `NaN`
-   空字符串（`""`）

当传递给条件语句所有其他的值，包括所有对象会被计算为真。

请不要混淆原始的布尔值`true`和`false` 与 [`Boolean`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Boolean)对象的真和假。例如：

```
var b = new Boolean(false);
if (b) //结果视为真
if (b == true) // 结果视为假
```

#### **示例**

在以下示例中，如果`Text`对象中的字符数为 3，函数`checkData`将返回`true`；否则，显示警报并返回`false`。

```
function checkData() {
  if (document.form1.threeChar.value.length == 3) {
    return true;
  } else {
    alert("Enter exactly three characters. " +
      document.form1.threeChar.value + " is not valid.");
    return false;
  }
}
```