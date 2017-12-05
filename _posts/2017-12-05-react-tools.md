---
layout: post
title:  "React源码中的工具方法"
date:   2017-08-17
excerpt: "React源码中定义和引用了一些工具方法，供各个模块调用."
tag:
- react 
comments: true
---

React源码中，引用和定义了一些基础的模块，用于兼容性判断、控制台报错等。

## [object-assign](https://github.com/sindresorhus/object-assign)

功能同[Object.assign](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/assign)，用于合并若干个对象。

考虑兼容性问题，该模块提供了ponyfill方案，适配常用浏览器以及nodejs环境。

## reactProdInvariant

用于报错，给出了错误详细信息的线上链接。

## canDefineProperty

判断当前环境是否支持[Object.defineProperty](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty)方法，等价于判断了当前环境的对象是否支持访问器属性（ES5）。

## lowPriorityWarning

用于控制台输出详细的报错信息，提供了插值逻辑（%s用作插值标记）。

## getIteratorFn

获得被传入的遍历器对象的遍历方法。

## [fbjs](https://github.com/facebook/fbjs)

### fbjs/lib/warning

用于控制台输出详细的报错信息，提供了插值逻辑（%s用作插值标记）。

### fbjs/lib/emptyObject

得到一个空对象。

### fbjs/lib/invariant

异常报警。



