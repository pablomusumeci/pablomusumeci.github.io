---
title:  Implementing LRU Cache in Python
excerpt: Goodness of Python's OrderedDict
last_modified_at: 2015-10-06
categories:
  - Python
  - Software Engineering
---

Just wanted to share this great [post](https://www.kunxi.org/blog/2014/05/lru-cache-in-python/). It basically talks about how we can implement an LRU Cache in Python using the advantages of the **OrderedDict** data structure.

Never heard of OrderedDict? I recommend you to look for [further information](https://docs.python.org/2/library/collections.html#collections.OrderedDict) about the structure itself and the things we can accomplish by using it.

Long story short:

> An OrderedDict is a dict that remembers the order that keys were first inserted. If a new entry overwrites an existing entry, the original insertion position is left unchanged. Deleting an entry and reinserting it will move it to the end.

This is not the only way to implement an LRU Cache efficiently, there is another way for achieving the same running time by using a [Hash Table and a Double Linked List](https://www.geeksforgeeks.org/implement-lru-cache/) to recreate the same functionality the OrderedDict is giving us here. This happens because we use the Hash Table for the quick lookup operation that checks if a key is in the cache or not, and the Double Linked List to keep track of the age of each key.
