---
layout: post
title: python中bytes和string的转换
---

## 起因
前几天使用python练习了如何进行TCP的信息传输，在使用的过程中，发现数据格式需要转换成```bytes```才可以正常地传输，但是在接收到信息后，又需要将```bytes```进行解码，转换成```string```才可以。因此，需要进行两者的相互转换。

## 转换
其实转换是很简单的。

如何将```string```转换成```bytes```：
```python
string_a = 'hello'
bytes_a = bytes(string_a, 'utf-8')
```

如果需要将```bytes```转换成```string```:
```python
string_a = str(bytes_a, 'utf-8')
```

## 说明
其实还有其他的转换方式，但是我觉得这样子使用起来是最方便、直观的，因此，我只记录这一种转换的方法。
