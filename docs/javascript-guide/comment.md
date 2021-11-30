# 注释

## 注释文本前加空格

```js
// bad
//mostly works on mobile browser
let connectionSource = connection.type;

// good
// mostly works on mobile browser
let connectionSource = connection.type;

// bad
/**
 *first initial index and indexCached have same value,
 *so this shall not triggered at the beginning
 */
if (current !== prevCurrent) {
  // ...
}

// good
/**
 * first initial index and indexCached have same value,
 * so this shall not triggered at the beginning
 */
if (current !== prevCurrent) {
  // ...
}
```

## 单行注释

```js
// bad
let responsive = {}; // DO NOT change this object variable name

// good
// DO NOT change this object variable name
let responsive = {};

// bad
function slider() {
  let index = 0;
  // DO NOT change this object variable name
  let responsive = {};

  // ...
}

// good
function slider() {
  let index = 0;

  // DO NOT change this object variable name
  let responsive = {};

  // ...
}

// also good
function slider() {
  // DO NOT change this object variable name
  let responsive = {};

  // ...
}
```

## 多行注释

```js
// bad

// responsive breakpoint list (min. width) :
//
//  base  => mobile
//  md    => 768 / small tablet
//  lg    => 1024 / large tablet
//  xl    => 1200 / desktop
//  xxl   => 1600 / large desktop

function slider() {
  // ...
}

// good

/**
 * responsive breakpoint list (min. width) :
 * base  => mobile
 * md    => 768 / small tablet
 * lg    => 1024 / large tablet
 * xl    => 1200 / desktop
 * xxl   => 1600 / large desktop
 */

function slider() {
  // ...
}
```

## 代码表达的意思很清楚的时候不用添加多余的注释了

```js
// bad
function isDeviceMobile() {
  const screenWidth = window.innerWidth;
  const mobileBreakpoint = 767.98;

  if (screenWidth <= mobileBreakpoint) {
    // if in range, return true
    return true;
  } else {
    // if not return false
    return false;
  }
}
```

## 特殊标记注释

有时候我们需要在代码中添加一些特殊的注释，增强我们的代码表达能力。

```js
// TODO   功能未完成，待完善
// FIXME  待修复
// HACK   此处写法有待优化
// BUG    此处有 Bug
function utils() {
  // ...
}
```

示例：

```js
// TODO 未处理IE6-8的兼容性
function setOpacity(node, val) {
  node.style.opacity = val;
}
```

## 文件注释

位于文件头部，一般包含概要、作者、版本改动信息以及修改时间等内容

```js
/*
 * 简述当前文件功能
 * @author 作者名称
 * @version 版本号 最近编辑时间
 * @description 该版本改动信息
 */
```

## 添加作者、时间

重要的模块、引用次数较多的代码应该添加作者、时间信息，以便于查找。

```js
/**
 * @Description: 计算a、b的和
 * @author 夏洁琼
 * @date 2021-11-29 21:03:00
 */
function sum(a, b) {
  // ...
}
```

## 相关 VSCode 插件

1. Better Comments

注释分类，更加人性化

2. TODO Highlight

高亮显示 TODO、FIXME、BUG 等注释
