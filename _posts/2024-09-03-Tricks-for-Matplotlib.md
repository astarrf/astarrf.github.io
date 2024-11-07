---
math: true  # enable math mode
title: Tricks for better looking Matplotlib drawing
#date: YYYY-MM-DD HH:MM:SS +0800
categories: [Note]
tags: [python,plot,note,en]     # TAG names should always be lowercase
---

## $\LaTeX$ and multi-line in all the texts
You can have $\LaTeX$ environment by simply add `r` before the text. If you want to have multi-line, you can do like below:
```python
text=r"First line""\n"r"Second line"
```
where you have to add `r` for both line to enable the $\LaTeX$ env.

## multi-columns in legend
Use `plt.legend(ncol=k)` where `k` is the number of columns you want.
