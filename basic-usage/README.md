# 基本使用

GitBook 的两条基本命令
```
$ gitbook init     // 初始化书籍目录
$ gitbook serve     // 编译书籍并启动本地web服务
```

创建书籍 gitbook-note GitBook 使用笔记
```
//创建一下目录
gitbook-note/
├── README.md
└── SUMMARY.md
```
README.md 和 SUMMARY.md 是两个必须文件

README.md 是对书籍的简单介绍，SUMMARY.md 是书籍的目录结构
SUMMARY.md的内容格式如下 
```
# Summary

* [介绍](README.md)
* [安装](install/README.md)
* [使用](basic-usage/README.md)
```
### 使用 `gitbook init` 初始化书记目录
```
$ gitbook init 
$ tree
.
├── README.md
├── SUMMARY.md
├── install
│   └── README.md
└── basic-usage
    └── README.md
```

### 使用 gitbook serve 编译书籍

```
$ gitbook serve
Live reload server started on port: 35729
Press CTRL+C to quit ...

info: 7 plugins are installed
info: loading plugin "livereload"... OK
info: loading plugin "highlight"... OK
info: loading plugin "search"... OK
info: loading plugin "lunr"... OK
info: loading plugin "sharing"... OK
info: loading plugin "fontsettings"... OK
info: loading plugin "theme-default"... OK
info: found 3 pages
info: found 5 asset files
info: >> generation finished with success in 1.7s !

Starting server ...
Serving book on http://localhost:4000

```
浏览器访问 `http://localhost:4000` 就可预览编译后的电子书, 效果如下图
![](/assets/snipaste_20171120_171704.png)

***
在编译过程中遇到下面这个问题。`no such file or directory`
这个问题在issues 上也有许多人遇到
https://github.com/GitbookIO/gitbook/issues/1309
```
$ gitbook serve
Live reload server started on port: 35729
Press CTRL+C to quit ...

info: 7 plugins are installed
info: loading plugin "livereload"... OK
info: loading plugin "highlight"... OK
info: loading plugin "search"... OK
info: loading plugin "lunr"... OK
info: loading plugin "sharing"... OK
info: loading plugin "fontsettings"... OK
info: loading plugin "theme-default"... OK
info: found 2 pages
info: found 1 asset files

Error: ENOENT: no such file or directory, stat 'D:\gitbook\Import\gitbook-note\_book\gitbook\gitbook-plugin-fontsettings\fontsettings.js',Error: ENOENT: no such file or directory, stat 'D:\gitbook\Import\gitbook-note\_book\gitbook\gitbook-plugin-fontsettings\website.css'
```
解决方法就是
* 将杀毒软件关了
![](/assets/snipaste_20171120_170532.png)

* 使用管理员身份运行命令
![](/assets/snipaste_20171120_170808.png)

***
