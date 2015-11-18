---
layout: post
title: Kadane's Algorithm
categories:
- Algorithm
- Python
tags:
- Algorithm
- Python
- Quant
---

## Kanane's algorithm

Kanane's algorithm 首先遍历这个array的值，在array的每个位置上，都计算一下最大的正的sum subarray。这个subarray要么是空的（sum=0），要么包括1个或者多个elements。

``` python
def max_subarray(A):
  max_ending_here = max_so_far = 0
  for x in A:
    max_ending_here = max(0,max_ending_here+x)
    max_so_far = max(max_so_far,max_ending_here)
   return max_so_far
```

