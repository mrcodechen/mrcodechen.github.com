---
layout: post
title: "使用javadoc生成api文档"
category: maven
tags: 
 - maven
 - javadoc
 - eclipse
---

## 使用Eclipse生成javadoc

1. 选择工程，在菜单Project->Genarate Javadoc
2. 选择工程，鼠标右键菜单Export，选择Java 下面的Javadoc，点”next” 按钮
3. 选择工程，在菜单File->Export，选择Java 下面的Javadoc，点”next” 按钮
4. 然后，可以选择生成到Javadoc 文档中的内容(一般选public 或protected)，选存放目录( 默认即可)，next下一步 
5. 此页全默认即可，再next下一步 
6. 此时如果项目采用的是UTF-8的编码，一定要在这一页的Extra Javadoc options 中加” -encoding UTF-8 -charset UTF-8 ″；否则生成的网页中文注释都是乱码；点 Finish 完成。

## 使用Maven生成javadoc
### 1. 插件的基本配置

<pre class="brush:xml">
<plugin>
    <groupId>org.apache.maven.plugins</groupId>  
    <artifactId>maven-javadoc-plugin</artifactId>  
    <version>2.9.1</version>  
</plugin>
</pre>

### 2. 执行Maven命令
使用mvn javadoc:javadoc [-pl 指定项目]命令生成
