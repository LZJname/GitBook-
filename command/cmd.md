# 命令信息 

**列出gitbook的所有命令**

```
gitbook help
```

**列出gitbook-cli的帮助信息**

```
gitbook --help
```

**列出gitbook版本**

```
gitbook ls //本地所有gitbook版本
gitbook ls-remote //远程所有可用的gitbook版本
```
**安装对应的gitbook版本**
```
gitbook fetch 标签/版本号
```
**更新到gitbook最新版本**
```
gitbook update
```
**卸载对应的gitbook版本**
```
gitbook uninstall 2.0.1
```
**指定log的级别**
```
gitbook build --log=debug
```
**输出错误信息**
```
gitbook build --debug 
```
**预览书籍**

使用下列命令运行一个服务器，通过<http://localhost:4000/>可以预览书籍

```
gitbook serve
```

运行后会在文件夹中生成一个```_book```的文件夹，里面为生成的html文件。

使用下列命令生成静态网页而不运行服务器

```
gitbook build
gitbook build --gitbook=2.0.1 //生成时指定gitbook的版本,本地没有会先下载
```

