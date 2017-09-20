## 插件
### background
### HTML CSS Class Completion
### VScode-icons
### HTML CSS Support
### HTML Snippets
### Debugger for Chrome
### vetur VueHelper
### JavaScript (ES6) code snippets 
### sass
### vscode-fileheader
### emmet





## 问题
- visual studio code中使用emmet插件在.vue文件失效

１、文件→设置，在右侧窗口添加以下代码：

```
"emmet.syntaxProfiles": {
        "vue-html": "html",
        "vue": "html"
    }


```
2、在.vue文件窗口的右下角，点击“vue"(提示信息：选择语言模式)，然后选择".vue"的配置文件关联，再选择html即可。

- VS code 保存时自动格式化的问题

        JS-CSS-HTML Formatter这个插件在捣蛋




## 快捷键

- 快速打开文件
ctrl+p 输入要打开的文件 

- eslint 检查Vue文件

```
// 将设置放入此文件中以覆盖默认设置
{
  "files.associations": {
   "*.vue": "vue"
  },
"editor.tabSize": 2,
"editor.detectIndentation": false,
"eslint.validate": [
   "javascript",
  "javascriptreact",
   "vue"
 ]
}
```


