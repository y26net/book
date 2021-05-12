* 常用命令

```
# 全局安装
$ npm i gitbook-cli -g

# 初始化gitbook
$ gitbook init

# 本地服务
$ gitbook serve

# 资源打包
$ gitbook build

# 署到 gh-pages 分支
$ npm install g gh-pages
$ gh-pages -d _book


指定路径：gitbook build [书籍路径] [输出路径]
指定端口：gitbook serve --port 2333
生成pdf格式：gitbook pdf ./ ./mybook.pdf
生成epub格式：gitbook epub ./ ./mybook.epub
生成 mobi 格式：gitbook mobi ./ ./mybook.mobi


# 案例
$ git clone https://github.com/y26net/book.git
$ cd book
$ gitbook init
$ gitbook serve
$ gitbook build
$ git add .
$ git commit -m 初始化book
$ git push  或 git push -u origin main
$ git subtree push --prefix=_book origin ph-pages
```



* 概述

```

README.md —— 书籍的介绍写在这个文件里

SUMMARY.md —— 书籍的目录结构在这里配置

```
