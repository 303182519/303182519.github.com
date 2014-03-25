---
layout: post
category : css
tagline: "项目无Bug之日即是下线之时"
title: 表格数据换行
---

## 表格数据换行


###长英文或者长字段换行写法总结如下:需要了解的3个属性

----------




- 1.word-wrap:break-word 词内换行 只支持连续的英文和数字，在表格中失效
- 2.word-break:break-all 边界内换行 支持包括英文和数字的词句短，在火狐中失效
- 3.table-layout:fixed 固定表格 启动该属性可在表格中支持word-wrap:break-word;overflow:hidden


###普通容器中（Div）的用法建议

----------

word-wrap:break-word;

###容器中（Div）中的表格的用法建议

----------

table-layout:fixed;word-wrap:break-word;