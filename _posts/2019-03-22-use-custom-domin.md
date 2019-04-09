---
layout: post
title:  Use Custom Domain 启用自定义域名
date:   2019-03-22 18:00:00 +0800
categories: diary
---
#### 背景
- 自己的云服务器马上就要到期，暂时并没有续费打算
- 低配服务器个人博客体验不好
- 维护困难，对于我日常想写点东西来讲，自己维护一个系统任务偏重


痛定思痛，决定把原来的域名也简单搬迁过来

> zengqiang.ren  

对这个域名一直情有独钟，搬迁过程很顺利，只需要修改域名 `cname` 记录，解析到自己的 `github io` 博客地址即可  
过程并不困难，简单梳理之

#### 步骤

1. 到域名后台修改域名 `CNAME`
2. 到 `github` 项目对应的 `settings` 里面修改自己的域名设置
3. 建议开启 https，直接勾选`Enforce https`即可，勾选完成之后因为新的证书需要签发，所以需要有**24小时**左右等待证书（实际上并不会这么久）
4. 修改自己主题的 `_includes/footer.html`，增加备案信息 **【重要】**

#### 部分参考

- 默认主题 [minima](https://github.com/jekyll/minima) 地址
- 配置自己的域名 [Using a custom domain with GitHub Pages](https://help.github.com/en/articles/using-a-custom-domain-with-github-pages)
- [jekyll](https://jekyllrb.com/) 工具
- [jekyll插件](https://github.com/topics/jekyll-plugin) 地址，比较实用的如：[jekyll admin](https://github.com/jekyll/jekyll-admin) 提供`CMS-style`管理控制台

#### 延伸

过程中也翻到了其他博客框架，如：[Hexo](https://hexo.io/zh-cn/)，但是因为时间不充分，并没有深入研究  
感谢开源世界给我力量🌹  
