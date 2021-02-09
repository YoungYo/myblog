# GitBook 入门指南

GitBook 是一款现代化的文档平台，支持团队协作，可以在上面写产品文档、内部知识分享、接口文档等。GitBook 有网页版和本地版两种，网页版地址如下：[https://www.gitbook.com/](https://www.gitbook.com/)，本地版地址如下：[https://github.com/GitbookIO/gitbook](https://github.com/GitbookIO/gitbook)。

本地版是基于 Node.js 开发的，所以需要本地安装 Node.js 环境，本地版现已停止维护了，而且本地版的大部分功能网页版都支持，所以本教程主要是介绍网页版的使用方式。

GitBook 和 GitHub 是什么关系呢？这是两个相互独立的网站，但是你在 GitBook 上创建的文档可以同步到 GitHub 仓库，每次对文档的修改都会生成一个 commit，GitBook 会自动帮你提交到 GitHub，这样有助于追溯历史版本。而你往 GitHub 提交的内容也会自动同步到 GitBook。（具体怎么在 GitBook 和 GitHub 之间建立关联一会儿会讲到，但是在这之前，我假设你已经会使用 GitHub 了，如果你没有，可以点击下方的链接获取相关教程。）

{% file src=".gitbook/assets/cong-0-kai-shi-xue-xi-github.pdf" %}

## 注册 GitBook 账号

打开 GitBook 网址后，点击「Sign Up」按钮注册一个 GitBook 账号，也可以直接用谷歌账号或者 GitHub 账号登录。

