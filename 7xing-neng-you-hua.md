## 自动化工具
### webpack
- HMR 

webpack --watch (监听文件变化自动编译，但不刷新)
webpack-dev-serve (要加query才能HMR)
webpack-dev-serve --contentbase src --inline --hot







- 缓存

 [缓存版本控制代码](localSdk.js)
 
- 自动刷新浏览器

```javascript

var gulp = require('gulp');
var browserSync = require('browser-sync').create(); // 静态服务器

// 浏览器重载
gulp.task('reload', browserSync.reload);

// 使用默认任务启动Browsersync，监听JS文件
gulp.task('default', function() {

    // 从这个项目的根目录启动服务器
    browserSync.init({
        server: {
            baseDir: "./"
        }
    });

    // 添加 browserSync.reload 到任务队列里
    // 所有的浏览器重载后任务完成。
    gulp.watch("**/js/*.js", ['reload']);
    gulp.watch("**/css/*.css", ['reload']);
    gulp.watch("**/*.html", ['reload']);
});

```
 