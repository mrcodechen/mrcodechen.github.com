---
layout: post
title: "Git实现从本地添加项目到远程仓库"
category: git
tags: 
 - git
 - ubuntu
---

## Git实现从本地添加项目到远程仓库

在github上创建项目：https://github.com/mrcodechen/mrcodechen.github.com

运行命令：
<pre class="brush: shell">
touch README.md
git init
git add README.md (git add . 为提交全部)
git commit -m "first commit"
git remote add origin https://github.com/mrcodechen/mrcodechen.github.com
git push -u origin master
</pre>
