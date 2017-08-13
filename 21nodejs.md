### 进击nodejs基础
#### url uri的区别
url:统一资源定位符(使用哪种协议访问资源)
uri:统一资源标识符(字符串格式规范)
uri包含url

#### node版本
第二位奇数为稳定版， 偶数为实验版



#### 测试性能
apctch ab
```
ab -n1000 -c10 http://www.imooc.com
```