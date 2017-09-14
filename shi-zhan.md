## 经验

- 抽象公用方法
- 抽象对象（es6类）

### css
1. 设计都有风格规范，颜色 字体
2. 一般包括index mixin base icon reset variable几个文件
3. 偏移用transform


## js
- 取整  0.7 | 0
- Math.max(0, x) 最小是0
- 获得数组副本    array.slice()
- api节流    debounce(原理延迟请求，再次触发清除上一个延迟)
- 控制快速切换    setTimeout(,1000) 并且在此之前清理timeout, 这样就可以只执行最后一个
- 取反    i=!i
- 逆转    message.split('').reverse().join('')


## 浏览器
- 浏览器17秒刷新一次， 所以用20s

## vue
- 生命周期，用v-if渲染避免
- 不需要双向绑定的值不要写在data props里




