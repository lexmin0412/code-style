# 格式

<!-- prettier-ignore-start -->
## 插件

格式化统一使用 prettier 插件，eslint 用作语法校验，同时关闭 eslint 中关于格式化的规则，防止和 prettier 冲突

## prettier 配置

.prettierrc.js

```js
module.exports = {
  bracketSpacing: true,
  singleQuote: true,
  trailingComma: "es5",
  arrowParens: "avoid",
  semi: false,
  printWidth: 120,
  tabWidth: 2,
};
```

### tabWidth: 2

单个 tab 的宽度，默认两个空格

```
// bad
function sum(a, b) {
    return a + b;
}

// good
function sum(a, b) {
  return a + b;
}
```

### singleQuote: true

使用单引号代替双引号

```js
// bad
const quote = "I am a string";

// good
const quote = 'I am a string';
```

### printWidth: 120

一行字符数超过 120 后换行

### bracketSpacing: true

对象括号间空格

```js
// bad
const obj = {a: 1}

// good
const obj = { a: 1 }
```

### trailingComma: "es5"

多行逗号分隔的语法结构中，使用尾逗号

```js
// bad
const obj = {
  a: 1,
  b: 2
}

// good
const obj = {
  a: 1,
  b: 2,
}
```

### semi: false

句尾去分号

```js
// bad
const obj = {
  a: 1,
  b: 2,
};
const a = 1;

// good
const obj = {
  a: 1,
  b: 2,
}
const a = 1
```

### arrowParens: "avoid"

箭头函数只有一个参数时不用加括号

```js
// bad
const foo = (x) => x * x;

// good
const foo = x => x * x;
```

### endOfLine: "lf"

统一行尾换行为 \n (LF换行)

<!-- prettier-ignore-end -->
