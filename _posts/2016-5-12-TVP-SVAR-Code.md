---
layout: post
title: TVP-SVAR 模型以及其MATLAB代码
categories:
- 模型
- 代码
tags:
- 模型
- Lingo
- 贝叶斯
- TVP-SVAR
- Gibbs
- State Space Model
---

TVP-SVAR模型，全称“Time Varying Structural Vector Autoregressions”，由Primiceri(2005)提出，用来对宏观经济变量进行建模，尤其是进行货币政策的研究。

关于这个模型的具体情况和估计方法，可以参考Time Varying Structural Vector Autoregressions and Monetary Policy（Primiceri，2005）。

这个模型最大的好处，就是允许模型系数和扰动项的方差协方差都是时变的。这也造成了估计上的难度。Primiceri（2005）采用了MCMC的方法来计算似然函数。然而，网上能找到的代码大多有这样那样的错误。这里提供一个带有数据的可以完美运行的MATLAB程序。[点击这里进行下载。](https://raw.githubusercontent.com/newhotter/cn/gh-pages/slides/TVP-SVAR_MATLAB_Code.zip)

模型估计最后所得到的结果图如下：

![](https://raw.githubusercontent.com/newhotter/cn/gh-pages/slides/results.jpg)

