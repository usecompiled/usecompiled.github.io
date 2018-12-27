---
title: Setting up a custom subdomain for your github page
date: 2018-12-27 08:30:39
category: blog
tags: githubpages
---

设置三级域名
-------------
在您的域名商网站对域名进行解析，`记录类型` 选择` CNAME`,主机记录填写您想使用的三级域名x `((x).example.com)`， `记录值`就是您的github page地址`username.github.io`，保存设置。


```bash
# 注意：主机目录中只需填写 x 即可。
```

设置github page的映射
---------------------------

在你的Github Page repository 创建 `CNAME`文件，内容为您所使用的完整的三级域名`((x).example.com)`。


**这一步我直接在库中创建CNAME 并配置，结果并没有映射成功通过查询，同时邮箱也收到了“Page build warning”，报错为：**

```c 
The page build completed successfully, but returned the following warning for the `master` branch:

The CNAME `git.1314933.com/` is not properly formatted. See https://help.github.com/articles/troubleshooting-custom-domains/#github-repository-setup-errors for more information.
```

通过查询，得出解决方案：

1. 打开Github Page所在的 Github 库，点击 settings
2. 在options选项卡中找到GitHub Pages
3. 在Custom domain中输入完整的三级域名，保存即可。


