# 概念
- 单线程 事件驱动 非阻塞io
- Node.js没有根目录的概念，因为它根本没有任何的web容器！


### 进击nodejs基础
#### url uri的区别
url:统一资源定位符(使用哪种协议访问资源)
uri:统一资源标识符(字符串格式规范)
uri包含url

#### node版本
第二位奇数为稳定版， 偶数为实验版



#### 测试性能
apache ab

```
ab -n1000 -c10 http://www.imooc.com
```


#### npm插件
- cheerio 解析html
- moment 时间格式化
- superagent    http request


### 会话持久化
1. 存到cookies里面
2. 存到redis
3. 存到mongodb(用connect-mongo)

#### 常见问题
- Cannot find module './build/Release/sharp'
    
    参考 https://github.com/nodejs/node-gyp#installation
        https://github.com/lovell/sharp/issues/598

- mysql要安装community server版本