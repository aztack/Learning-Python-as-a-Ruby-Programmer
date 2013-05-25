学好Python内置函数！
===================

列出所有内置函数:`[fn for fn in dir(__builtins__) if fn[0].islower()]`
(其中包含一些非函数的)

[内置函数列表](http://docs.python.org/2.7/library/functions.html)

数学、数字相关
--------------

```python
abs
divmod
max
min
pow
round
sum

hex
oct

float
int
long
complex
cmp
```

abs:
```python
abs(1) == 1
abs(-3) == -3
abs(-3.14) == 3.14
abs(complex(3,4)) == 5.0
```

cmp:
```python
cmp(1,1) == 0
cmp(1,2) == -1
cmp(2,1) == 1
cmp('a','b') == -1
cmp('aa','ab') == -1
```


列表、序列、字符串、字典相关
--------

```python
list
dict
len
str

```


类型相关
--------
str
list
dict

IO相关
------

执行环境相关
------------
