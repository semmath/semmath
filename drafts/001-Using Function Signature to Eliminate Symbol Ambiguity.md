---
title: Using Function Signature to Eliminate Symbol Ambiguity
author: 青羽
date: 2024.11.24
version: 0.1.0
state: draft
---

# 现状

$\sin^{-1}(x)$ 是表示 $\frac{1}{sin(x)}$ 还是 $\arcsin(x)$ 呢？（x 的类型是一个实数，sin，arcsin 是函数名，下同）

没有标准答案。表示什么取决于不同的上下文，这有点像编程语言中的多态，但又不是真正的多态。真正的多态是可以通过规则分析明确语义的。但是数学里的 $\sin^{-1}(x)$ 在不提供上下文之前根本无法找到确定的解释，就算提供了上下文也不一定能自洽，比如根据上下文解释说这里是反函数，那么 $\sin^{-2}(x)$ 又表示什么呢？这种情况下通常又解释成幂了。这里就出现了矛盾：同是实数类型，在同一个位置上说明语义应该是一致的，-1 表示反函数，-2 就表示幂，这很矛盾并且不自洽。

$\sin^{-2}(x)$ 的作用就像一个函数：`power(sin(x), -2)`，但是 $\sin^{-1}(x)$ 的作用就像 `arcsin(x)`。类似的例子不胜枚举。

# 解决方案

$\sin(x)$ 通常值域是实数域，针对一个函数 $f()$ ，这个函数的参数是两个实数 $x$ 和 $y$ ，作用是得到 $x^y$ 也就是 $x$ 的 $y$ 次幂，那么 $f(\sin(x), -1)$ 可以写作 $\sin^{-1}(x)$ 表示的就应该是 $\sin(x)$ 的-1 次幂。

至于反函数，反函数本质上和倒数是不一样的，是两个不同的函数，不应该用原函数的-1 次幂的写法，那是一种错误。所以如果表示 $\sin(x)$ 的反函数，就应该写 $\arcsin(x)$ ，只有在表示幂的时候，才用右上角上标的写法。否则， $\sin^{2}(x)$ 就表示 $\sin(\sin(x))$ 了（如果要采用这套体系来解释的话，也不是不可以，重点是要统一）。

本质上，角标的位置代表了函数参数的位置，角标上的那个数代表了函数参数的类型，函数名称、函数参数的位置（个数）和其对应的类型共同构成函数签名，而函数签名是唯一决定该函数语义的东西。
