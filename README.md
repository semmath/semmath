# Semantic Mathematics Specification

[中文](README_zh.md)

## Brief

"Semantic Mathematics" or "SemMath" contains a set of rules and requirements that specify how to write mathematical symbols, aiming to standardize the mathematical notation system and improve the accuracy and readability of mathematical articles.

### Why?

- Eliminate symbol ambiguity

  The same symbol may have different meanings in different contexts. For example, does $\sin^{-1}(x)$ represent $\frac{1}{sin(x)}$ or $\arcsin(x)$? SemMath avoids possible confusion in understanding through clear rules.

- Resolve symbol conflicts

  In the field of mathematics, there are often situations where there are not enough symbols or conflicts between symbols, such as finding that all commonly used symbols have been used up while writing, and having to use various complex variants -- cursive, bold, double-lined, etc. -- which are often difficult to distinguish at a glance. SemMath adopts the naming convention in the computer field, which can solve the problem of symbol conflicts. Not only does it make the symbols more intuitive and easy to understand, but it also allows for easy writing in environments without $\LaTeX$.

### When?

- When working with others or facing the public.
- When writing math-related articles on computers.

### How?

- It's still under development at this stage, so you may need to read all the drafts to make sure you understand the rules.
- After the 1.0.0 version is released, you only need to read the articles in standards.
- In the later stage, we will consider developing dedicated open source software to automatically detect and update the symbol systems in existing mathematical articles; Type validity verification and variable name auto-completion are performed during writing articles.

## Status

CreateDate: 2024.11.24

Version: 0.0.3

Under development. Many things waiting to be done.

## Contribution

### 0. Organization

You can apply to join the [semmath development team](https://github.com/semmath) through email or private message, and become a member of the development team after approval.

The following steps apply to those who are not members of the development team.

### 1. Issues

Propose a discussion in the Issues.

If the modifications are quite clear and concise, you can skip this step.

### 2. Pull Requests

Submit Pull Requests.

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

For the overall framework, considering the current scale, any good ideas can be directly submitted (after discussion) for changes. Whenever the overall framework undergoes phased updates, the patch version number or minor version number of the "SemMath" will be correspondingly incremented. Once the overall framework becomes basically stable and the content is essentially complete, version 1.0.0 will be released, and the "standards" directory will be enabled. Stable and complete articles will transition from the `draft` status to the `standard` status.

### 3. Merge

After confirmation by the members of the development team, the changes will be merged into the main branch.
