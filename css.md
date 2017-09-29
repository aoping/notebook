# 参考链接
Mark Otto 编写的HTML/CSS代码风格指南    http://hao.jobbole.com/htmlcss-code-guide-by-mark-otto/



# 原则
- 最大程度复用css,少写相同的代码
- 面向属性命名
- 三无原则 无id 无层级 无标签
- JS专用class选择器名以 .js- 为前缀；
- 单一功用class名以 .u- 为前缀，如 .u-underline、.u-capitalize 等；
- 引入有意义的连字符和驼峰法，以此强调元件、子元件、修改器名的分隔；
- 状态类class（一般由JS来控制）名以 .is- 为前缀，如 .is-disabled 等；
- 使用新的CSS变量名规则： [属性]-[值]--[元件] ；
- 混写只在万不得已的补漏时出现，只能以 .m- 作为前缀。

# 架构
## 关于reset
不需要全部重置，只需要重置部分标签即可

```
body{
    line-height:1.4;
    color:#333;
    font-family:arial;
    font-size: 12px;
    background:white;
}
input,textarea,select{
    font-size:100%;    
    font-family:inherit;
}
body,h1,h2,h3,h4,h5,h6,p,ul,ol,form{
    margin:0;
}
h4,h5,h6{
    font-size:1em;
}
ul,ol{
    padding-left:0; 
    list-style-type:none;
}
/*image with no-border*/
img{border:0;}
```



### 边距

  移动端左右30px    左右是上下的1.5倍

### fontsize lineheight
h5 28px 40px
h4 32px 45px
h3 45px  60px
h2 60px 100px
h1 80px 120px





# 布局
## 显示器分辨率
- desktop 1920*1080
- laptop  

## 流动性（自适应）布局

## 固定布局

## 内部元素随最外层变化，只需要改变最外层即可



# tips
- 内外标签如果高度一样，不要同时出现相同的定值
- 命名可以参照BEM，但是没必要严格遵守





