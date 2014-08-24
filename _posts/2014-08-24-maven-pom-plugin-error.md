---
layout: post
category: maven
title: "解决Maven报Plugin execution not covered by lifecycle configuration"
tags: 
 - maven
 - eclipse
---

## 解决Maven报Plugin execution not covered by lifecycle configuration 

在 &lt;plugins&gt; 标签外再套一个 &lt;pluginManagement&gt; 标签:
<pre class="brush:xml">
&lt;build&gt;
    &lt;pluginManagement&gt;
        &lt;plugins&gt;
            &lt;plugin&gt; ... &lt;/plugin&gt;
            &lt;plugin&gt; ... &lt;/plugin&gt;
                  ....
        &lt;/plugins&gt;
    &lt;/pluginManagement&gt;
&lt;/build&gt;
</pre>

问题解决。

----