### 常用特性
- 解构赋值

- 箭头函数

- set和map

- 异步操作

- 类与对象

- 模块化


### 知识点
es6默认开启"use strict"
Object.assign()浅拷贝
Set主要用于去重
Proxy主要用于拦截
Proxy和Reflect用于验证
class 构造函数 get set 继承 静态方法(static) 静态属性
自己部署iterator接口， 可以自己写也可以用generator定义
generator yield返回的是iterator类型， 可以实现状态机（async和await是generator的语法糖）
第三方库修饰器的js库：core-decorators; npm install core-decorators
修饰器用于埋点

#### 解构赋值


#### 正则表达式


#### 字符串
- padStart 可以用于日期补白 1->01
- repeat 用于重复
- 字符串模板
- codePointAt fromCodePoint 用于处理编码大于\xFFFF的字符
- include startsWith endsWith 处理字符串是否保护
- 标签模板    处理多语言切换i18n 处理html防止攻击
- raw

#### 数值

```
console.log(0b111110111)
console.log(0o767)
```
- Math.sign() 符号
- Math.trunc() 取整舍弃小数部分
- 

#### 数组




#### 模块化
- export import

```

export let A = 1
export function B() {

}

export class C{

}
export default {
    A,
    B,
    C
}

import {A, B, C} from ''
import * as D from ''
import D from ''

```



