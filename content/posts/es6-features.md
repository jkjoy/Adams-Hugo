---
title: "JavaScript ES6+ 新特性概览"
date: 2023-12-28T11:30:00+08:00
draft: false
tags: ["JavaScript", "ES6", "编程"]
categories: ["技术"]
thumbnail: "https://picsum.photos/seed/js/400/300"
---

ECMAScript 6（ES6）及后续版本为 JavaScript 带来了许多强大的新特性。

## let 和 const

块级作用域变量声明：

```javascript
let x = 10;
const PI = 3.14159;
```

<!--more-->

## 箭头函数

简洁的函数语法：

```javascript
const add = (a, b) => a + b;
const greet = name => `Hello, ${name}!`;
```

## 模板字符串

```javascript
const name = "World";
console.log(`Hello, ${name}!`);
```

## 解构赋值

```javascript
// 数组解构
const [a, b] = [1, 2];

// 对象解构
const {name, age} = {name: "Alice", age: 25};
```

## 展开运算符

```javascript
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5];

const obj1 = {a: 1};
const obj2 = {...obj1, b: 2};
```

## Promise

处理异步操作：

```javascript
fetch('/api/data')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error(error));
```

## async/await

更优雅的异步代码：

```javascript
async function fetchData() {
  try {
    const response = await fetch('/api/data');
    const data = await response.json();
    return data;
  } catch (error) {
    console.error(error);
  }
}
```

## 类

面向对象编程：

```javascript
class Person {
  constructor(name) {
    this.name = name;
  }

  greet() {
    console.log(`Hello, I'm ${this.name}`);
  }
}
```

## 模块

```javascript
// 导出
export const name = "Module";
export default function() {}

// 导入
import defaultExport, {name} from './module.js';
```

这些特性让 JavaScript 开发更加现代化和高效！
