异步编程技术使你的程序可以在执行一个可能长期运行的任务的同时继续对其他事件做出反应而不必等待任务完成。与此同时，你的程序也将在任务完成后显示结果。

浏览器提供的许多功能（尤其是最有趣的那一部分）可能需要很长的时间来完成，因此需要异步完成，例如：

-   使用 [`fetch()`](https://developer.mozilla.org/zh-CN/docs/Web/API/fetch "fetch()") 发起 HTTP 请求
-   使用 [`getUserMedia()`](https://developer.mozilla.org/zh-CN/docs/Web/API/MediaDevices/getUserMedia "getUserMedia()") 访问用户的摄像头和麦克风
-   使用 [`showOpenFilePicker()` (en-US)](https://developer.mozilla.org/en-US/docs/Web/API/Window/showOpenFilePicker "Currently only available in English (US)") 请求用户选择文件以供访问

因此，即使你可能不需要经常_实现_自己的异步函数，你也很可能需要_正确使用_它们。

在这篇文章中，我们将从同步函数长时间运行时存在的问题开始，并以此进一步认识异步编程的必要性。

## [同步编程](https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/Asynchronous/Introducing#同步编程 "Permalink to 同步编程")

同步程序就是你正常写代码

观察下面的代码：

```
const name = 'Miriam';
const greeting = `Hello, my name is ${name}!`;
console.log(greeting);
// "Hello, my name is Miriam!"
```

这段代码：

1.  声明了一个叫做 `name` 的字符串常量
2.  声明了另一个叫做 `greeting` 的字符串常量（并使用了 `name` 常量的值）
3.  将 `greeting` 常量输出到 JavaScript 控制台中。

我们应该注意的是，实际上浏览器是按照我们书写代码的顺序一行一行地执行程序的。浏览器会等待代码的解析和工作，在上一行完成后才会执行下一行。这样做是很有必要的，因为每一行新的代码都是建立在前面代码的基础之上的。

这也使得它成为一个**同步程序**。

事实上，调用函数的时候也是同步的，就像这样：

```
function makeGreeting(name) {
  return `Hello, my name is ${name}!`;
}
const name = 'Miriam';
const greeting = makeGreeting(name);
console.log(greeting);
// "Hello, my name is Miriam!"
```

在这里 `makeGreeting()` 就是一个**同步函数**，因为在函数返回之前，调用者必须等待函数完成其工作。