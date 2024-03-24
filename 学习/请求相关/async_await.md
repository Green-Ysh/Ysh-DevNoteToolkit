# async/await 是什么？

`async/await` 是 JavaScript 中处理异步操作的一种语法糖。它使得编写异步代码更加简洁和易读。

# 如何使用 async/await？

要使用 `async/await`，首先需要将函数标记为 `async`。然后，在需要等待异步操作完成的地方，使用 `await` 关键字。

下面是一个示例：

```javascript
/**
 * 使用 Fetch API 从指定的 URL 获取数据，并将响应数据记录到控制台。
 * @async
 * @function fetchData
 * @throws {Error} 如果获取数据时发生错误。
 */
async function fetchData() {
  try {
    const response = await fetch("https://api.example.com/data");
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error("Error fetching data:", error);
  }
}

// 调用 fetchData 函数
fetchData();
```
