# Gitbook安装

## 说明
gitbook是一个很漂亮、上档次的做笔记的工具  
> 官网：https://www.gitbook.com/ (需要注册)

## linux(命令行)配置安装三步骤
- sudo apt-get install -y nodejs(node -v 验证是否安装成功)
- sudo apt-get install -y npm
- npm install gitbook-cli -g(可能需要fq；gitbook -V 验证是否安装成功)

## gitbook最基本的组织结构
### README.md
这个文件相当于一本Gitbook的简介，最上层(和SUMMARY.md同级)的是本书的Introduction。
### SUMMARY.md
这个文件是一本书的目录结构，使用Markdown语法，修改它相当于更新书籍目录,SUMMARY.md举例：  
```java
* [基本安装](howtouse/README.md)
 - [Node.js安装](howtouse/Nodejsinstall.md)
 - [Gitbook安装](howtouse/gitbookinstall.md)
 - [Gitbook命令行速览](howtouse/gitbookcli.md)
* [图书编辑](book/README.md)
 - [gitbook命令行&markdown编辑](book/gitbook-cli.md)
 - [gitbook editor编辑](book/editor.md)
* [图书输出](output/README.md)
 - [输出为静态网站](output/outfile.md)
 - [输出PDF](output/pdfandebook.md)
* [发布](publish/README.md)
  - [发布到gitbook.com](publish/gitbook.md)
  - [Github集成](publish/github.md)
  - [发布到Github Pages](publish/gitpages.md)
* [结束](end/README.md)
```
- 可以看到，**每个目录中，都有一个README.md文件，相当于一章的说明。**
- 一旦改动了summary文件，通过运行‘gitbook init’命令能够在***对应各级目录***下生成*对应的md文件*
- 往往改动后需要实时查看效果，那么可以运行‘gitbook serve’，然后打开固定[链接](http://localhost:4000)就能直观看见当前行文结构啦
- 除了各级readme，其他普通md文件都是你接下来要写的具体文章哦(**markdown一定要会，否则白扯**)

### 其他命令
```
$ gitbook -h

  Usage: gitbook [options] [command]

  Commands:

    build [options] [source_dir] Build a gitbook from a directory
    serve [options] [source_dir] Build then serve a gitbook from a directory
    install [options] [source_dir] Install plugins for a book
    pdf [options] [source_dir] Build a gitbook as a PDF
    epub [options] [source_dir] Build a gitbook as a ePub book
    mobi [options] [source_dir] Build a gitbook as a Mobi book
    init [source_dir]      Create files and folders based on contents of SUMMARY.md
    publish [source_dir]   Publish content to the associated gitbook.io book
    git:remote [source_dir] [book_id] Adds a git remote to a book repository

  Options:

    -h, --help     output usage information
    -V, --version  output the version number
```
### 我总结的发布流程
1、github创建一个空仓库，例如/notebook
2、本地clone下上面的仓库
3、利用gitbook 本地命令行初步构建整个summary
4、push 至远程仓库
5、以后都只需在github网页端 **在线编辑**每个md文件即可

### 课题
- 不会用github，不懂git基本使用，请参考xx
- GitBook.com 其实还可以集成 GitHub，这里不具体讲，详见xx
- 后续github上的任何文章的更新，都能通过‘git pull’命令同步到本地哦
