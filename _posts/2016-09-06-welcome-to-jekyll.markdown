---
layout: post
title:  "Welcome to Jest!"
date:   2016-09-06 13:31:33 +0800
---
### Jest安装
局部安装
`npm install --save-dev jest` 

全局安装 
`npm install -g jest`

### 测试
**假设被测试文件为sam.js，内容如下**

```
function sum(a, b) {
  return a + b;
}
module.exports = sum;
```

**测试文件为sam.test.js，内容如下**

```
test('adds 1 + 2 to equal 3', () => {
  const sum = require('../sum');
  expect(sum(1, 2)).toBe(3);
});
```

**修改package.json文件**

```
"scripts": {
  "test": "jest"
}
```

**运行 `npm test`**

### Notes

**1. 可以在package.json中添加对jest的配置，如**

```
"jest": {
    "testEnvironment": "node",
    "collectCoverage": "true"
 }
``` 
* `testEnvironment` 指定测试环境，

* `collectCoverage:true` ，系统会自动创建coverage文件夹，在coverage/lcov-report/ 文件夹中可看到被测试文件覆盖情况（未被覆盖代码行高亮显示）

**2. 测试文件命名**
* 如sum.test.js，遵循XXX.test.js或者XXX.spec.js，可放在任意位置
* 放在`__tests__`文件夹内的XXX.js文件

**3. jest命令**
* 全局安装，可直接运行，如 `jest --coverage`

* 局部安装，需在bin目录下运行，如 `./node_modules/.bin/jest --coverage`

***
> https://facebook.github.io/jest/

