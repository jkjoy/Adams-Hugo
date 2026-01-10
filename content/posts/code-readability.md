---
title: "如何提高代码可读性"
date: 2023-12-20T09:15:00+08:00
draft: false
tags: ["编程", "最佳实践", "代码规范"]
categories: ["技术"]
thumbnail: "https://picsum.photos/seed/code/400/300"
---

可读性是衡量代码质量的重要标准之一。好的代码应该易于理解和维护。

## 命名规范

### 使用有意义的变量名

❌ 不好：
```javascript
const d = new Date();
const x = users.filter(u => u.a);
```

✅ 好：
```javascript
const currentDate = new Date();
const activeUsers = users.filter(user => user.isActive);
```

<!--more-->

## 函数设计

### 单一职责原则

每个函数只做一件事：

```javascript
// 不好 - 函数做了太多事情
function processUser(user) {
  validateUser(user);
  saveToDatabase(user);
  sendEmail(user);
  updateCache(user);
}

// 好 - 分解为小函数
function registerUser(user) {
  if (!isValidUser(user)) return;

  saveUser(user);
  notifyUser(user);
  refreshUserCache(user);
}
```

## 注释

### 写有用的注释

```javascript
// 不好 - 注释重复代码
// 设置 x 为 5
let x = 5;

// 好 - 解释为什么
// 根据A/B测试结果，5秒是最佳超时时间
const OPTIMAL_TIMEOUT = 5000;
```

## 代码格式化

### 保持一致的缩进和空格

使用工具如 Prettier 自动格式化代码。

## 避免深层嵌套

```javascript
// 不好
if (user) {
  if (user.isActive) {
    if (user.hasPaid) {
      // do something
    }
  }
}

// 好 - 提前返回
if (!user) return;
if (!user.isActive) return;
if (!user.hasPaid) return;

// do something
```

## 使用现代语法

```javascript
// 不好
var items = [];
for (var i = 0; i < data.length; i++) {
  items.push(data[i].name);
}

// 好
const items = data.map(item => item.name);
```

## 错误处理

明确的错误处理：

```javascript
async function fetchUserData(userId) {
  try {
    const response = await api.getUser(userId);
    return response.data;
  } catch (error) {
    logger.error('Failed to fetch user', {userId, error});
    throw new UserFetchError(userId);
  }
}
```

记住：代码是写给人看的，顺便让计算机执行！
