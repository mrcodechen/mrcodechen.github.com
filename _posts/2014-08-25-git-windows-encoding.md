---
layout: post
title: "解决Windows下Git Bash中文乱码问题"
category: git
tags: 
 - git
---

### 1.编辑git安装目录/etc/gitconfig文件最下面添加：
<pre class="brush:xml">
	[gui]
		encoding = utf-8
	[i18n]
		commitencoding = GB2312
</pre>

### 2.编辑git安装目录/etc/git-completion.bash文件最下面添加：

alias ls='ls --show-control-chars --color=auto'

### 3.编辑git安装目录/share/vim/vimrc文件最下面添加：

<pre class="brush:xml">
	set fenc=utf-8
	set encoding=utf-8
	set fileencodings=ucs-bom,utf-8,cp936
	set fileencoding=utf-8
	set termencoding=gbk
</pre>
