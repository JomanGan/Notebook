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

>\* [基本安装](howtouse/README.md)  
> \- [Node.js安装](howtouse/Nodejsinstall.md)  
> \- [Gitbook安装](howtouse/gitbookinstall.md)  
> \- [Gitbook命令行速览](howtouse/gitbookcli.md)  
>\* [图书编辑](book/README.md)  
> \- [gitbook命令行&markdown编辑](book/gitbook-cli.md)  
> \- [gitbook editor编辑](book/editor.md)  
>\* [图书输出](output/README.md)  
> \- [输出为静态网站](output/outfile.md)  
> \- [输出PDF](output/pdfandebook.md)  
>\* [发布](publish/README.md)  
>  \- [发布到gitbook.com](publish/gitbook.md)  
>  \- [Github集成](publish/github.md)  
>  \- [发布到Github Pages](publish/gitpages.md)  
>\* [结束](end/README.md)  


