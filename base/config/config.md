# 配置
记录Gitbook的一些配置信息

* [title - 标题](#title)
* [author - 作者信息](#author)
* [description - 书本描述](#description)
* [language - 使用的语言](#language)
* [gitbook - 指定gitbook版本](#gitbook)
* [root - 指定存放 GitBook 文件的根目录](#root)
* [links - 在侧边栏添加链接](#links)
* [styles - 自定义样式](#styles)
* [plugins - 插件](#plugins)
* [pluginsConfig - 插件配置](#pluginsconfig)
* [structure - 设置 Readme, Summary, Glossary等对应的文件](#structure)

## title
设置书本的标题
```json
"title" : "Gitbook Use"
```

## author
作者的相关信息
```json
"author" : "zhangjikai"
```

## description
本书的简单描述
```json
"description" : "记录Gitbook的配置和一些插件的使用"
```

## language
Gitbook使用的语言, 版本2.6.4中可选的语言如下：
```
en, ar, bn, cs, de, en, es, fa, fi, fr, he, it, ja, ko, no, pl, pt, ro, ru, sv, uk, vi, zh-hans, zh-tw
```
配置使用简体中文
```
"language" : "zh-hans",
```
## gitbook
指定使用的gitbook版本
```json
"gitbook" : "3.2.2",
"gitbook" : ">=3.0.0"
```
## root
指定存放 GitBook 文件（除了 book.json）的根目录
```json
"root": "."
```
## links
在左侧导航栏添加链接信息
```json
"links" : {
    "sidebar" : {
        "Home" : "http://zhangjikai.com"
    }
}
```

## styles
自定义页面样式， 默认情况下各generator对应的css文件
```json
"styles": {
    "website": "styles/website.css",
    "ebook": "styles/ebook.css",
    "pdf": "styles/pdf.css",
    "mobi": "styles/mobi.css",
    "epub": "styles/epub.css"
}
```
例如使`<h1> <h2>`标签有下边框， 可以在`website.css`中设置
```css
h1 , h2{
    border-bottom: 1px solid #EFEAEA;
}

```
## plugins
配置使用的插件
```
"plugins": [
    "disqus"
]
```
添加新插件之后需要运行`gitbook install`来安装新的插件  

Gitbook默认带有5个插件：
* highlight
* search
* sharing
* font-settings
* livereload

如果要去除自带的插件， 可以在插件名称前面加`-`
```json
"plugins": [
    "-search"
]
```
## pluginsConfig
配置插件的属性
```json
"pluginsConfig": {
    "fontsettings": {
        "theme": "sepia",
        "family": "serif",
        "size":  1
    }
}
```
## structure
指定 Readme、Summary、Glossary 和 Languages 对应的文件名，下面是这几个文件对应变量以及默认值：

| 变量 | 含义和默认值 |
|:----|:----|
|`structure.readme` | `Readme file name (defaults to README.md)` |
|`structure.summary` | `Summary file name (defaults to SUMMARY.md)`|
|`structure.glossary`| `Glossary file name (defaults to GLOSSARY.md)` |
|`structure.languages`| `Languages file name (defaults to LANGS.md)`|

## bookjson样例

```
{
    "title": "GitBook 使用教程",
    "description": "记录 GitBook 的配置和一些插件的使用",
    "author": "zhangjikai",
    "output.name": "site",
    "language": "zh-hans",
    "gitbook": "3.2.3",
    "root": ".",
    "structure": {
        "readme": "introduction.md"
    },
    "links": {
        "sidebar": {
            "Home": "http://www.zhangjikai.com"
        }
    },
    "plugins": [
        "-lunr",
        "-search",
        "-highlight",
        "-livereload",
        "search-plus@^0.0.11",
        "simple-page-toc@^0.1.1",
        "github@^2.0.0",
        "github-buttons@2.1.0",
        "edit-link@^2.0.2",
        "disqus@^0.1.0",
        "prism@^2.1.0",
        "prism-themes@^0.0.2",
        "advanced-emoji@^0.2.1",
        "anchors@^0.7.1",
        "include-codeblock@^3.0.2",
        "ace@^0.3.2",
        "emphasize@^1.1.0",
        "katex@^1.1.3",
        "splitter@^0.0.8",
        "mermaid-gb3@2.1.0",
        "tbfed-pagefooter@^0.0.1",
        "expandable-chapters-small@^0.1.7",
        "sectionx@^3.1.0",
        "donate@^1.0.2",
        "local-video@^1.0.1",
        "sitemap-general@^0.1.1",
        "anchor-navigation-ex@0.1.8",
        "favicon@^0.0.2",
        "todo@^0.1.3",
        "3-ba@^0.9.0",
        "terminal@^0.3.2",
        "alerts@^0.2.0",
        "include-csv@^0.1.0",
        "puml@^1.0.1",
        "musicxml@^1.0.2",
        "klipse@^1.2.0",
        "versions-select@^0.1.1",
        "rss@^3.0.2",
        "-sharing",
        "sharing-plus@^0.0.2",
        "graph@^0.1.0",
        "chart@^0.2.0"
    ],

    "pluginsConfig": {
        "theme-default": {
            "showLevel": true
        },
        "disqus": {
            "shortName": "gitbookuse"
        },
        "prism": {
            "css": [
                "prism-themes/themes/prism-base16-ateliersulphurpool.light.css"
            ]
        },
        "github": {
            "url": "https://github.com/zhangjikai/gitbook-use"
        },
        "github-buttons": {
            "repo": "zhangjikai/gitbook-use",
            "types": [
                "star"
            ],
            "size": "small"
        },
        "include-codeblock": {
            "template": "ace",
            "unindent": true,
            "edit": true
        },
        "sharing": {
           "douban": false,
           "facebook": false,
           "google": true,
           "hatenaBookmark": false,
           "instapaper": false,
           "line": false,
           "linkedin": true,
           "messenger": false,
           "pocket": false,
           "qq": false,
           "qzone": false,
           "stumbleupon": false,
           "twitter": false,
           "viber": false,
           "vk": false,
           "weibo": true,
           "whatsapp": false,
           "all": [
               "facebook", "google", "twitter",
               "weibo", "instapaper", "linkedin",
               "pocket", "stumbleupon", "qq", "qzone"
           ]
       },
        "tbfed-pagefooter": {
            "copyright": "Copyright © zhangjikai.com 2017",
            "modify_label": "该文件修订时间：",
            "modify_format": "YYYY-MM-DD HH:mm:ss"
        },
        "3-ba": {
            "token": "ff100361cdce95dd4c8fb96b4009f7bc"
        },
        "donate": {
            "wechat": "https://zhangjikai.com/resource/weixin.png",
            "alipay": "https://zhangjikai.com/resource/alipay.png",
            "title": "",
            "button": "赏",
            "alipayText": "支付宝打赏",
            "wechatText": "微信打赏"
        },
        "simple-page-toc": {
            "maxDepth": 3,
            "skipFirstH1": true
        },
        "edit-link": {
            "base": "https://github.com/zhangjikai/gitbook-use/edit/master",
            "label": "Edit This Page"
        },
        "sitemap-general": {
            "prefix": "http://gitbook.zhangjikai.com"
        },
        "anchor-navigation-ex": {
            "isRewritePageTitle": false,
            "tocLevel1Icon": "fa fa-hand-o-right",
            "tocLevel2Icon": "fa fa-hand-o-right",
            "tocLevel3Icon": "fa fa-hand-o-right"
        },
        "sectionx": {
            "tag": "b"
        },
        "favicon": {
            "shortcut": "favicon.ico",
            "bookmark": "favicon.ico"
        },
        "terminal": {
            "copyButtons": true,
            "fade": false,
            "style": "flat"
        },

        "versions": {
            "options": [
                {
                    "value": "http://gitbook.zhangjikai.com",
                    "text": "v3.2.3"
                },
                {
                    "value": "http://gitbook.zhangjikai.com/v2/",
                    "text": "v2.6.4"
                }
            ]
        },

        "rss": {
            "title": "GitBook 使用教程",
            "description": "记录 GitBook 的配置和一些插件的使用",
            "author": "Jikai Zhang",
            "feed_url": "http://gitbook.zhangjikai.com/rss",
            "site_url": "http://gitbook.zhangjikai.com/",
            "managingEditor": "me@zhangjikai.com",
            "webMaster": "me@zhangjikai.com",
            "categories": [
                "gitbook"
            ]
        }
    }
}
```

