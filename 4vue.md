### 组件通信

1，父组件将一个数据props赋给两个子组件,并是sync的，子组件watch数据回调。

2.event bus
vue2.0里面的event bus(其实就是个发布订阅模式)：

```
var bus = new Vue()

// in component A's method
bus.$emit('id-selected', 1)

// in component B's created hook
bus.$on('id-selected', function (id) {
  // ...
})
```
新建 bus.js:

import Vue from 'vue'
export var bus = new Vue()
再在组件里面： import bus from 'bus.js'


3.$dispatch $broadcast
建议不用，2.0要废除

4.vuex

5.$refs
```
一定要有0
this.$refs['chiild'][0].method()

```



