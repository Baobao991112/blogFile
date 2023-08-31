---
title: 使用Map数据类型来渲染列表
date: 2023-08-29 14:48:42
tags:
---

## Map 数据类型的定义

new Map() 是 JavaScript 中的内置数据结构，用于存储键值对的集合。使用 new Map() 可以创建一个空的 Map 对象。

使用 Map 对象的主要优势是它提供了高效的键值对存储和查找操作。与普通的 JavaScript 对象相比，Map 对象具有以下一些特点和优势：

键可以是任意类型：Map 对象的键可以是任意类型的值，包括原始类型（如字符串、数字）和对象。而普通的 JavaScript 对象的键只能是字符串或符号。
保持插入顺序：Map 对象会记住插入键值对的顺序，因此可以按插入顺序来迭代键值对。
快速的查找和删除操作：Map 对象提供了快速的查找和删除操作，时间复杂度为 O(1)。
可迭代：Map 对象是可迭代的，可以使用 for...of 循环或 forEach 方法遍历键值对。
在给定的代码 const cache = new Map(); 中，new Map() 被用来创建一个名为 cache 的新的空 Map 对象。这个 Map 对象可以用来存储和检索键值对，提供了高效的数据操作和遍历方法。

使用 Map 对象通常是因为它提供了更灵活和高效的键值对存储和操作，适用于需要频繁插入、查找和删除键值对的场景。

## Map 的基本操作

```javaScript
    const data = new Map()
    添加/修改
    data.set(1,'obj') // { 1 => 'obj'}
    data.set(2,'obj2') // { 1 => 'obj' , 2 => 'obj2'}
    删除
    data.delete(1) // {2 => 'obj2'}
```

## Map 渲染列表

```javaScript
    const data = new Map();
    data.set(1, 'A');
    data.set(2, 'B');
    data.set(3, 'C');

    const divContainer = document.getElementById('div-container');

    data.forEach((value, key) => {
        const div = document.createElement('div');
        div.textContent = value;
        divContainer.appendChild(div);
    });
```
