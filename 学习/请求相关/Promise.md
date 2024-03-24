# Promise 是什么？

Promise 是 JavaScript 中处理异步操作的一种机制。它代表了一个**异步操作**的最终完成或失败，并可以返回一个值。

# 如何使用 Promise？

使用 Promise 可以通过以下步骤来处理异步操作：

1. 创建一个 Promise 对象，传入一个执行器函数，该函数接受两个参数：resolve 和 reject。
2. 在执行器函数中，执行异步操作，并在操作完成时调用 resolve 方法来表示操作成功，或调用 reject 方法来表示操作失败。
3. 使用 then 方法来处理操作成功的情况，使用 catch 方法来处理操作失败的情况。

以下是一个简单的示例：

```javascript
const promise = new Promise((resolve, reject) => {
  // 在此处执行异步操作
  // 如果操作成功，调用 resolve()
  // 如果操作失败，调用 reject()
});

promise
  .then((result) => {
    // 此处处理成功操作
  })
  .catch((error) => {
    // 此处处理失败操作
  });
```
