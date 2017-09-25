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

- Array.of() 创建数组
- Array.from([], function) 把类数组转换成数组， map
- [].fill() 填充
- [].keys() [].values() [].entries()
- [].copyWithin(0,1,2)
- find findIndex
- includes


#### 函数
- 函数默认值
```
function a(x, y = 'world'){
    console.log(x,y)
}
```
- 作用域问题
```
let x = '111'
function a(x, y = x){
    console.log(x,y)
}

a('222')  // 222,222 块作用域

```
- res参数    把离散值转换成数组

```
function a(...res){
    for(let s of res) {
        console.log(s)
    }
}

```

- 扩展运算符    把数组转换成离散值
console.log(...[1,2,3])


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
- 箭头函数
- 尾调用（函数的最后是不是函数）？？？？？
主要用于递归优化



#### 对象
- 简洁写法

```
let o = {
 a,
 b
}

let o={
    hello() {
        console.log(1)
    }
}

let a = 'b'
let o = {
 [a]: '1'
}

```

- Object.is() 相当于===
- Object.assign() 浅拷贝
** 注意：只是拷贝对象的引用地址，不会拷贝继承的属性， 不会拷贝不可枚举的属性**
- 扩展运算符（babel对其支持不友好）



#### Symbol(提供独一无二的值)

```
let a1 = Symbol()
let a2 = Symbol()
console.log(a1===a2) // false
let a3 = Symbol.for('a3') // 赋值
let a4 = Symbol.for('a3') // 取值
console.log(a3===a4) // true

let a = Symbol.for('abc')
let o= {
    [a]: 1,
    'abc': 2,
    'c': 3
}

```

**注意用let in/of是取不到Symbol的，要用Object.getOwnPropertySymbols(obj),想遍历所有属性要用Reflect.ownKeys(obj)**


#### Set Map
**优先使用Map，要求唯一使用Set**

- Set与数组    **Set中的元素不能重复**
- Set WeakSet    WeakSet值只能是对象，没有.size 不能遍历 不能clear
```
let a = new Set()
a.add(1)
a.add(2)
a.has(1)
a.delete(1)
a.clear()
console.log(a.size) //注意是size而不是length

let arr = [1,2,3,4,5]
let b = new Set(arr)

// 去重
let arr = [1,2,3,4,5,1,2]
let b = new Set(arr)




```

- Map与对象    Map的key可以是任意类型，对象的key只能是字符串或Symbol
- Map WeakMap WeakMap的key只能是对象，没有.size 不能遍历 不能clear

```
let map = new Map()
let arr = ['123']
map.set(arr, 456)
map.delete(arr)
map.clear()

console.log(map,map.get(arr),map.size) // 取值


let map = new Map([['a',123],['b',456]])
console.log(map,map.get('a')) // 取值


```


#### Proxy和Reflect
- get set has ownKeys 
- 用于校验解耦 要重点看!!!!!!!
```


```

#### class
- 定义
- 继承 extends
- getter setter
- 静态方法static（通过类调用）
- 静态属性在类外定义 class.static


#### Promise
- all 表示把多个promise当作一个promise,当所有promise状态都改变了，all的状态才改变
```
Promise.all([

])
```

- race 只要有一个状态改变



#### Iterator for...of
- for...of 是遍历实现了iterator

**数组已经实现了iterator, 对象没有实现**
- 数组的iterator
```
let arr=['hello', 'world']
let map=arr[Symbol.iterator]() // 有next方法
console.log(map.next()) // {value: 'hello', done: false}
console.log(map.next()) // {value: 'world', done: false}
console.log(map.next()) // {value: undefined, done: true} done为true时循环停止


```
- 对象部署iterator
```
let obj = {
  data: [ 'hello', 'world' ],
  [Symbol.iterator]() {
    const self = this;
    let index = 0;
    return {
      next() {
        if (index < self.data.length) {
          return {
            value: self.data[index++],
            done: false
          };
        } else {
          return { value: undefined, done: true };
        }
      }
    };
  }
};
```

#### generator 解决异步编程的问题, 状态机

**async await是generator的语法糖**

```
let g=function* (){
    yeild 1
    yeild 2
    return 3
}
let k=g()
console.log(k.next()) // {value: 1, done:false}
console.log(k.next()) // {value: 2, done:false}
console.log(k.next()) // {value: 3, done:true}
console.log(k.next()) // {value: undefind, done:true}


// 注意next返回的都是{value, done}
// generator 返回的是iterator
```

```
let obj = {};
obj[Symbol.iterator]= function* () {
    yeild 1
    yeild 2
    yeild 3
}

for(let value of obj){
    console.log(value)
}
```
- 状态机
```
let state= function* () {
    while(1){
        yeild 1
        yeild 2
        yeild 3
    }
}
let status=state()
console.log(status.next())
console.log(status.next())
console.log(status.next())
console.log(status.next())

```

- async await
```
let state= async function() {
    while(1){
        await 1
        await 2
        await 3
    }
}
let status=state()
console.log(status.next())
console.log(status.next())
console.log(status.next())
console.log(status.next())

```







