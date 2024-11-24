# Semantic Mathematics Specification

[中文](README_zh.md)

## Brief

"Semantic Mathematics" or "SemMath" contains a set of rules and requirements for how to write mathematical symbols (when using computers), aimed at standardizing the mathematical symbol system, eliminating symbol ambiguity, reducing reading barriers, and improving the accuracy and readability of mathematical articles.

## Current Status

CreateDate: 2024.11.24

Version: 0.0.2

Under development. Many things waiting to be done.

## Contribution

1. Propose a discussion in the Issues.

If the modifications are quite clear and concise, then there is no need to discuss them.

2. Submit Pull Requests.

For the specific content of the specification, adopt a similar method to [RFC](https://www.rfc-editor.org/) as the following:

- Each proposal forms a draft article and is placed in the [drafts](./drafts/) directory.
- The article adopts the [Markdown](https://www.markdownguide.org/) format.
- The filename follows the format of `xxx-This is the Title.md`, where `xxx` is a three digit integer increasing from `001`.
- Each article begins with 5 lines of metadata:

  ```yml
  ---
  title: This is the Title
  author: Somebody
  date: 1970.01.01
  version: 0.1.0
  status: draft
  ---
  ```

- Each article has its own version, independent of the "SemMath" version.

Regarding the overall framework, given the current scale, any good ideas can be directly submitted (after discussion) for changes. Whenever the overall framework undergoes phased updates, the patch version number or minor version number of the "SemMath" will be correspondingly incremented. Once the overall framework becomes basically stable and the content is essentially complete, version 1.0.0 will be released, and the "standards" directory will be enabled. Stable and complete articles will transition from the `draft` status to the `standard` status.

3. After passing, it can merge into the main branch.
