# 命名规范

## 驼峰命名

方法名、参数名、成员变量、局部变量都统一使用 lowerCamelCase 风格，必须遵从驼峰形式。

```js
// bad
let _name;
let name_;
let name$;

// good
let firstName;
let lastName;
```

## 常量

大写，以下划线隔开

```js
// good
const HOUSE_TYPE = "4";
const POSTER_VIDEO = "20";
```

## 函数

前缀应为动词

|  动词  |       含义       |
| :----: | :--------------: |
|   is   | 判断是否为某个值 |
|  get   |    获取某个值    |
|  set   |    设置某个值    |
| handle |   处理某件事情   |
|   on   |       回调       |
|  use   |   常用于 hook    |
| create |       创建       |
| update |       更新       |
| delete |       删除       |
|  add   |       添加       |
|  find  |       查找       |
| search |       搜索       |
| clear  |       清除       |
| fetch  |     请求数据     |

```js
// good
function onSubmit() {}

function getName() {}

function isValid() {}

function useInterval() {}

function updateUserInfo() {}

function createUser() {}

function findUser() {}

function addUser() {}
```

## 类

首字母大写

私有属性加 \_ 前缀

```js
// good
class Person{
  public name;
  private _age;

  getName(){}
  setName(){}
}
```

## 变量

见名思意

```js
// bad
const d = 365;

// good
const aYearDays = 365;
```

避免模棱两可的名字

```js
// bad
const list = [{ id: 1, name: "john" }];

// good
const userList = [{ id: 1, name: "john" }];
```

## 函数

使用描述性的名字

```js
// bad
function calculate(a, b) {
  return a + b;
}

// good
function sum(a, b) {
  return a + b;
}
```
