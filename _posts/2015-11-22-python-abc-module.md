---
title:  Python ABC module
excerpt: Abstract Base Class module
last_modified_at: 2015-11-22
categories:
  - Python
  - Software Engineering
---

I want to mention something that can help you to reduce the amount of error prone class hierachies in Python.

This module comes as a part of the Python Standard Library and it is named [ABC](https://docs.python.org/2/library/abc.html).

This module is not going to assure you a bug-free code (I think that there is no single tool or technique that can guarantee that, do not forget that we live in a world that has no Silver Bullets) but it can assist you on detecting 2 types of errors quicker.

This errors are:

- Instanciating an abstract class
- Forgetting to write the code of an interface method

This extra safety can be quite useful given the fact that we don't have a compiler taking care of those kind of things like if we were coding in a statically typed language. I know this doesn't replace a compiler **at all**, but some extra help (or safety if you want to call it that way) is always welcomed.

[Here you have an excelent introduction for this module.](https://dbader.org/blog/abstract-base-classes-in-python)

PS: Thanks to [Alejandro García Marra](https://github.com/alegmarra) for spell checking and editing my posts.
