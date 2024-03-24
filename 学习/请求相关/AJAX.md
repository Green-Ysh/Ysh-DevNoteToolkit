# AJAX 使用文档

## 什么是 AJAX？

AJAX 是一种在无需重新加载整个网页的情况下，能够更新部分网页的技术。全称是 Asynchronous JavaScript And XML（异步 JavaScript 和 XML）。

## 如何使用 AJAX？

在 JavaScript 中，我们可以使用 XMLHttpRequest 对象来实现 AJAX。

以下是一个基本的 AJAX 请求示例：

```JavaScript
// 创建一个XMLHttpRequest对象
var xhr = new XMLHttpRequest();

// 打开一个GET请求，请求地址为'https://api.******.com/data'，异步请求
xhr.open('GET', 'https://api.******.com/data', true);

// 监听xhr对象的状态变化事件
xhr.onreadystatechange = function () {
  // 当请求完成且响应状态为200时
  if (xhr.readyState == 4 && xhr.status == 200)
    // 弹出响应内容
    alert(xhr.responseText);
}

// 发送请求
xhr.send();
```

## 如何使用 POST 方法的 AJAX 请求？

以下是一个使用 POST 方法的 AJAX 请求的示例：

```javascript
// 创建一个XMLHttpRequest对象
var xhr = new XMLHttpRequest();

// 打开一个POST请求，请求地址为"https://api.******.com/data"，异步方式
xhr.open("POST", "https://api.******.com/data", true);

// 设置请求头的Content-Type为"application/json"
xhr.setRequestHeader("Content-Type", "application/json");

// 监听xhr对象的状态变化事件
xhr.onreadystatechange = function () {
  // 当xhr对象的状态为4（请求已完成）且状态码为200（请求成功）时，弹出响应内容
  if (xhr.readyState == 4 && xhr.status == 200) alert(xhr.responseText);
};

// 发送请求，将数据转换为JSON字符串并作为请求体发送
xhr.send(JSON.stringify({ key: "value" }));
```

在这个示例中，我们创建了一个新的 XMLHttpRequest 对象，然后使用 open 方法初始化一个新的请求。这个方法接受三个参数：请求的类型（如 'GET' 或 'POST'），请求的 URL，以及是否异步执行请求。

然后，我们定义了 onreadystatechange 事件处理器。当 readyState 属性改变时，就会触发这个处理器。如果 readyState 为 4（表示请求已完成），并且 status 为 200（表示服务器的响应是成功的），那么我们就弹出一个包含服务器响应的警告。

最后，我们使用 send 方法发送请求。

## 注意事项

AJAX 请求可能会受到同源策略的限制。如果你尝试从不同的源（域名、协议或端口）请求数据，那么你的请求可能会被阻止。为了解决这个问题，你可以使用 JSONP 或 CORS。
在使用 AJAX 时，应该始终对服务器的响应进行错误处理。你可以通过检查 status 属性来实现这一点。
由于 AJAX 请求是异步的，所以你不能在请求完成之前使用从服务器返回的数据。你应该在回调函数中使用这些数据。