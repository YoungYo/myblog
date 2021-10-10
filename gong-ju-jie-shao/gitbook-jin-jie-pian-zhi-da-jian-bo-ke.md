# GitBook 进阶篇之搭建博客

这篇文章的由来是，前几天有位读者看了我的那篇[《GitBook 入门指南》](https://blog.supermouse.cn/gitbook-ru-men-zhi-nan)，然后来问我 GitBook 怎么配置自定义域名，当时我都不知道 GitBook 有这个功能，所以就研究了一下，发现利用自定义域名，完全可以搭建自己的博客，而且超级简单（所以你会发现本文的篇幅很短）。所以我就把这个过程整理了一下，分享给大家。在此也感谢这位读者提供的灵感。

阅读本文时，我假设你对 GitBook 有一个基本的了解，如果你没有的话，建议先看一下我的这篇文章：[《GitBook 入门指南》](https://blog.supermouse.cn/gitbook-ru-men-zhi-nan)。

## 注册域名及域名解析设置

在搭建博客之前，你需要有一个域名，让别人能通过这个域名访问到你的博客。注册域名可以选择[阿里云万网](https://wanwang.aliyun.com/?spm=5176.19720258.J\_8058803260.44.7c6a2c4a354tVs)或者其他域名服务商。域名注册完之后可能还需要实名认证或者备案啥的，你按照网站上的提示进行操作就行。

你注册的是一级域名，类似于 supermouse.cn、google.com 这样的，而在 GitBook 上配置的必须是二级域名，比如 blog.supermouse.cn 或者 mail.google.com 这样的。

以阿里云为例，你的域名准备妥当之后，点击右侧的「解析设置」。

![](https://tva1.sinaimg.cn/large/008eGmZEly1gnigql4373j31b205sgmg.jpg)

在解析设置页面，点击「添加记录」按钮

![](https://tva1.sinaimg.cn/large/008eGmZEly1gnigqma0zuj31w80q2tee.jpg)

在添加记录的页面，按照下图进行配置，记录类型选择「CNAME」；在主机记录输入框中输入一个二级域名，理论可以随便输如，但是最好输入一个望文生义的域名，比如 blog；解析线路选择默认就好；记录值输入框输入「hosting.gitbook.io」，这是 GitBook 的域名，假设你的域名是 blog.supermouse.cn，那么当你访问 blog.supermouse.cn 时，实际上访问的是 hosting.gitbook.io。TTL 是域名解析信息在 DNS 中的存在时间，选择默认的 10 分钟就好。最后点击「确认」按钮。

![](https://tva1.sinaimg.cn/large/008eGmZEly1gnigql8uzvj30lj0qt0tx.jpg)

## GitBook Space 配置自定义域名

打开 GitBook 的其中一个 Space

![](https://tva1.sinaimg.cn/large/008eGmZEly1gnigqoh8dkj324a0u0tcs.jpg)

然后点击左侧菜单栏中的「Advance」，再点击「Custom Domain」中的「Configure」按钮，在弹出的对话框中输入你之前在解析设置页面填写的域名，然后点击「Next」

![](https://tva1.sinaimg.cn/large/008eGmZEly1gnigqnsmqqj30po0sytac.jpg)

![](https://tva1.sinaimg.cn/large/008eGmZEly1gnigqlhbjuj30xe0kigmx.jpg)

这一步是说让你在域名解析设置的时候，记录类型选择 CNAME，记录值填 hosting.gitbook.io，这个我们前面已经设置过了，所以直接点击「Next」

![](https://tva1.sinaimg.cn/large/008eGmZEly1gnigqndndyj30xc0j6t9t.jpg)

![](https://tva1.sinaimg.cn/large/008eGmZEly1gnigqovfqtj30xa0ha0tj.jpg)

当出现以下提示的时候，说明域名配置成功了。然后我们点击「Done」

![](https://tva1.sinaimg.cn/large/008eGmZEly1gnigwh5adgj30xa0h8q3x.jpg)

然后在浏览器中打开一个新的标签页，输入我们自己的域名，就可以dkui访问 GitBook 中我们的 Space 了。这样，一个博客就搭建起来了。

![](https://tva1.sinaimg.cn/large/008eGmZEly1gnigqq7kp7j31eo0u043i.jpg)

国内用户要想直接访问你的 GitBook，必须得 fq 才行，但是通过自定义域名的方式，即使不用 fq，也可以访问到。虽然这样搭建的博客没有什么花哨的功能，但是界面很简洁，搭建过程也不复杂，适合不喜欢折腾的朋友。况且，我们写博客是为了分享知识，输出观点，相比于博客的功能和外表而言，我觉得博客的内容更重要。

不过这种方式也有一个缺点，就是一个域名只能对应一个 Space，如果你想让别人通过一个域名访问到你的多个 Space，可能还需要做一些额外的工作。比如写一个服务，让域名指向这个服务，别人访问域名时，这个服务返回一个页面，上面是你的两个 Space 的链接。不过这样就需要写代码，还得自己准备服务器。喜欢折腾的朋友可以尝试一下。
