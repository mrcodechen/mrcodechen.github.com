---
layout: post
category: maven
title: "mvn打包时跳过test的方法"
tags: 
 - maven
---

## mvn打包时跳过test的方法


我们有时因为测试不能运行,或者为了更快的 编译,希望用mvn package的时候跳过test,使用下面的方法就可以搞定了第一种方法:
<pre class="brush: shell">
mvn -DskipTests clean package
</pre>
第二种方法
<pre class="brush: shell">
mvn -Dmaven.test.skip=true clean package
</pre>

