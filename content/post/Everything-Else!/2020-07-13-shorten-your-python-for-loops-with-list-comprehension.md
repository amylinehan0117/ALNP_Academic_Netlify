---
title: Shorten your Python for loops with list comprehension
author: Nellie Ponarul
date: '2020-07-13'
slug: shorten-your-python-for-loops-with-list-comprehension
categories:
  - Other
tags:
  - Python
authors: ["nponarul"]
---

For loops can be lengthy, and I like to keep my code concise. In Python, you can use lists to shorten up for loop code into one line lists. For example, if I wanted to create a list that had the squares of another list, I can:


```python
import numpy as np

l = [1,2,3,4,5]
squares = []
for n in l:
    squares.append(n**2)

print(squares)
```

    [1, 4, 9, 16, 25]


Or, I can do this:


```python
squares = [n**2 for n in l]
print(squares)
```

    [1, 4, 9, 16, 25]


A great way to save space!
