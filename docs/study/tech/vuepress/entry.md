# 零基础入门需要的基本知识

## Markdown 基础语法

[markdown](https://spec.commonmark.org/)是一种轻量级标记语言，学起来非常方便。大家只要对着写，很快就能上手。你也可以学学[简易版教程](https://www.runoob.com/markdown/md-tutorial.html)

markdown 语法，大多数要求行首+字符组合+空格。

重点要学习的内容如下：

1. 标题

用 `# 标题内容` ，#越多标题字体越小

```md
# h1 Heading

## h2 Heading

### h3 Heading

#### h4 Heading

##### h5 Heading

###### h6 Heading
```

2. 段落

用空行分隔实现换行

```md
段落一

段落二

段落三
这会接着段落三
```

3. 列表

有序列表，用 `数字.空格`

```md
1. 有序列表一
2. 有序列表二
3. 有序列表三
```

无序列表，用 `-空格`

```md
- 无序列表一
- 无序列表二
- 无序列表三
```

4. 链接

文字链接，用 `[链接文字](链接地址)`

```md
[cecilpeng 的程序员生活](https://cecilpeng.github.io/)
```

图片链接，用 `![图片说明](链接地址)`

```md
![VuePress Logo](https://vuepress.vuejs.org/hero.png)
```

5. 表格

使用 | 来分隔不同的单元格，使用 - 来分隔表头和其他行

对齐方式：左对齐-:，居中对齐:-:，右对齐-:

```md
| 左对齐 | 右对齐 | 居中对齐 |
| :----- | -----: | :------: |
| 单元格 | 单元格 |  单元格  |
| 单元格 | 单元格 |  单元格  |
```

## Markdown 拓展

VuePress 基于 markdown-it，大家可以参考[基础语法](https://markdown-it.github.io/)。

重点要学习的内容如下：

1. 链接拓展

绝对路径相对于 vuepress 的当前工作目录，即 docs 目录

REAMDE.md 是默认地址，如/study 等价于/study/README.md

可以跳转到特定标题，如/study/vuepress/entry/#Markdown 拓展

2. 注意内容

```md
::: tip 自定义提示标题
这是一个提示
:::

::: warning 自定义警告标题
这是一个警告
:::

::: danger 自定义危险标题
这是一个危险警告
:::

::: details 自定义详情标题
这是一个详情块，在 IE / Edge 中不生效
:::
```

如果你还是觉得不够，那就看看[VuePress的Markdown拓展](https://vuepress.vuejs.org/zh/guide/markdown.html#header-anchors)

