# 目录结构

gitbook的基本目录结构如下

```
.
├── book.json  //存放配置信息
├── README.md 
├── SUMMARY.md //存放文件目录信息，默认为SUMMARY.md中，可在book.json更改
├── chapter-1/
|   ├── README.md
|   └── something.md
└── chapter-2/
    ├── README.md
    └── something.md
```

**Summary**

概要文件，主要存放Gitbook文件目录信息，一般默认对应文件为SUMMARY.md，可以在book.json重新定义该文件的对应值，它的一般格式为

```
# Summary

### Part I

* [Introduction](README.md)
* [Content](part1/content.md)

## Part II
* [Content](part2/content.md)

----  //这是一个水平分割线

* [last part](part3/end.md)

```



**Glossary**

词汇表文件，默认对应的文件为```GLOSSARY.md```。该文件主要存储词汇信息，如果其他页面中出现该文件中的词汇，鼠标放到词汇上会给出词汇示意，格式如下

```
## Git
分散式版本控制软件

## Markdown
Aaron Swartz 跟John Gruber共同设计的排版语言
```

