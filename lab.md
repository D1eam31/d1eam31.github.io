---
layout: learning
title: Jekyll Learning Lab
permalink: /lab/
---

# 我的第一个自定义 Layout 实验

这个页面用来帮助我理解 Jekyll 的构建过程。

## 当前页面经历了什么？

当前文件是：

`lab.md`

它首先指定：

`layout: learning`

因此 Jekyll 会寻找：

`_layouts/learning.html`

而 `learning.html` 又通过：

{% raw %}
`{% include learning-note.html %}`
{% endraw %}

引用了：

`_includes/learning-note.html`

最后，Markdown 正文经过解析后被放入：

{% raw %}
`{{ content }}`
{% endraw %}

的位置。

## 我的理解

Jekyll 并不是简单地把 Markdown 转换成 HTML。

它还负责把内容、模板和可复用组件组合起来，最终生成完整网页。