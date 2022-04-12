---
title: "概率论与数理统计学习笔记"
author: "李凯"
date: "2022-04-12"
output:
  html_document:
    df_print: paged
site: bookdown::bookdown_site
documentclass: elegantbook
bibliography:
- book.bib
- packages.bib
lot: yes
lof: yes
colorlinks: yes
toccolor: Maroon
link-citations: yes
nocite: '@*'
mathspec: yes
graphics: yes
subject: 基于 elegantbook 文类的 bookdown 模版
keywords:
- 概率与数理统计
- 笔记
- R语言
hyperrefoptions:
- linktoc=all
- pdfstartview=FitH
github-repo: XiangyunHuang/ElegantBookdown
classoption:
- lang=cn
- 11pt
- scheme=chinese
- chinesefont=nofont
- citestyle=gb7714-2015
- bibstyle=gb7714-2015
description: 最初看到 elegantbook 做的书籍样式很漂亮，就想把它引入到 bookdown 中，遂定制了此模版。在此基础上，做了迁移和扩展的工作，融合了
  LaTeX (精美)、Pandoc (简洁) 和 R (强大) 的特性。This is a bookdown template based on ElegantBook.
  The output format for this template is bookdown::gitbook and bookdown::pdf_book.
creator:
- role: author
  text: John Smith
- role: editor
  text: Sarah Jones
identifier:
- scheme: DOI
  text: doi:xxx
publisher: xx 出版社
rights: © 2019-2021 黄湘云 \& 叶飞, CC BY-4.0
ibooks:
  version: 0.7
subtitle: 用R实现概率论与数理统计
---

\mainmatter

# 简介 {-}



在学习机器前，需要对概率论与数理统计的指示进行学习。

所以本笔记是`Machine Learning with R`的基础。

本笔记主要跟随宋浩老师的[概率论与数理统计课程](https://www.bilibili.com/video/BV1ot411y7mU)进行学习。

一些符号：

1. `m`：表示样本数量

2. `x`：表示输入变量、特征变量

3. `y`：表示输出变量、目标变量

# 自定义 block {-}

基于 Pandoc 自定义 block 是一件很有意思的事情，目前不想让模版过于复杂，仅给出几个最常用的例子。如何自定义可以去看谢益辉的新书 <https://bookdown.org/yihui/rmarkdown-cookbook/custom-blocks.html>。

[要做的还有很多]{.todo}

::: {.rmdwarn data-latex="{警告}"}
这是警告
:::

::: {.rmdtip data-latex="{提示}"}
这是提示
:::

:::: {.rmdnote data-latex="{注意}"}
这是注意
::::

::: {.rmdinfo}
普通说明
:::


