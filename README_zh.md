# 语义化数学规范

[English](README.md)

## 简介

“语义化数学” 或 "SemMath" 包含一组规则和要求，规定（在计算机上）如何书写数学符号，旨在规范数学符号体系，消除符号歧义，降低阅读门槛，提高数学文章的准确性和易读性。

## 当前状态

创建日期: 2024.11.24

当前版本: 0.0.2

开发中。百废待兴。

## 贡献

1. 在 Issues 区提出讨论。

若是相当明了简洁的修改，可以省略讨论。

2. 提交 Pull Requests。

对于规范的具体内容，采取类似 [RFC](https://www.rfc-editor.org/) 的模式进行开发：

- 每个提案形成一个草稿文章（draft），放入 [drafts](./drafts/) 目录下。
- 文章采用 [Markdown](https://www.markdownguide.org/) 格式写成。
- 文件名采用格式：`xxx-This is the Title.md`，其中`xxx`是从`001`开始递增的三位整数。
- 每篇文章开头有 5 行元信息：

  ```yml
  ---
  title: This is the Title
  author: Somebody
  date: 1970.01.01
  version: 0.1.0
  status: draft
  ---
  ```

- 每篇文章有各自的版本，和“SemMath”版本独立。

对于整体的框架形式，考虑到当前规模，有好的想法（讨论后）直接提交更改即可。每次整体的框架形式有阶段性更新时，“SemMath”的修订版本号或次版本号进行对应的增加。当整体的框架形式基本稳定且内容基本完备之后，发布 1.0.0 版本，并启用 “standards” 目录，稳定且完备的文章由 `draft` 状态变更为 `standard` 状态。

3. 通过后可并入主分支。
