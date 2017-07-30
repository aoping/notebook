## 像素单位

- px 逻辑像素， 浏览器使用的抽象单位， 根据设备可大可小
- dp, pt 设备无关像素
- dpr 设备像素比
 1px = (dpr)^2 *dp
 
 iphone5 640dp*1136dp 320px*568px
 
 首先是有 dp 然后是dpr 最后是 px
 
- dpi 打印机每英寸可以喷的墨汁点
- ppi 屏幕每英寸的像素数量， 即密度， 越高越清晰
目前在计算机显示设备参数描述上， 二者意思一样

 计算公式 iphone5 iphone5是4英寸
 ppi = √ （1136^2 + 640^2)/4 = 326ppi （视网膜retina屏）
 
注意：ppi越高，像素数越高，图像越清晰，但可视度越低， 系统默认设置缩放比越大
![](/assets/TIM截图20170730155045.png)


## viewport
- ios viewport 980px   android 不固定
- visual viewport(视口viewport)

- layout viewport(布局viewport) 

## 1px边框


## flex布局 响应式布局


 ## 用tap代替click
 tap一般时间小于200ms, tap会有点透bug, 与300ms有关， 解决方案
 1. 使用缓动动画， 过渡300ms的延迟
 2. 上下都用tap事件
 3. 使用fastclick
 click时间大于300ms
 
 ## android touch bug
 android只会触发一次touchstart, 一次touchmove, touchend不触发
 解决方案： e.preventdefault
 
 ## 弹性滚动
 - body层自带弹性滚动
 
 
 - 局部滚动(android不支持，可以使用iscroll库)
 body{
 overflow: scroll;
 -webkit-overflow-scrolling: touch;
 }
 
 ## 
 
 
 
 