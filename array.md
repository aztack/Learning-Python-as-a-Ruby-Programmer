Array(list)
===========

Python中对应Ruby中的Array的数据结构叫list
Ruby中一些非常常用的Array和Hash的方法都来自Enumerable:

```ruby
irb(main):011:0> Enumerable.instance_methods
=> [:to_a, :entries, :sort, :sort_by, :grep, :count, :find, :detect, :find_index, :find_all, :select, :reject, :collect,
 :map, :flat_map, :collect_concat, :inject, :reduce, :partition, :group_by, :first, :all?, :any?, :one?, :none?, :min, :
max, :minmax, :min_by, :max_by, :minmax_by, :member?, :include?, :each_with_index, :reverse_each, :each_entry, :each_sli
ce, :each_cons, :each_with_object, :zip, :take, :take_while, :drop, :drop_while, :cycle, :chunk, :slice_before]
```

而在Python中没有对应的Enumerable。类似的方法都以内置方法实现：

```python
>>> [fn for fn in  dir(__builtins__) if fn[0].islower()]
['abs', 'all', 'any', 'apply', 'basestring', 'bin', 'bool', 'buffer', 'bytearray', 'bytes', 'callable', 'chr', 'classmet
hod', 'cmp', 'coerce', 'compile', 'complex', 'copyright', 'credits', 'delattr', 'dict', 'dir', 'divmod', 'enumerate', 'e
val', 'execfile', 'exit', 'file', 'filter', 'float', 'format', 'frozenset', 'getattr', 'globals', 'hasattr', 'hash', 'he
lp', 'hex', 'id', 'input', 'int', 'intern', 'isinstance', 'issubclass', 'iter', 'len', 'license', 'list', 'locals', 'lon
g', 'map', 'max', 'memoryview', 'min', 'next', 'object', 'oct', 'open', 'ord', 'pow', 'print', 'property', 'quit', 'rang
e', 'raw_input', 'reduce', 'reload', 'repr', 'reversed', 'round', 'set', 'setattr', 'slice', 'sorted', 'staticmethod', '
str', 'sum', 'super', 'tuple', 'type', 'unichr', 'unicode', 'vars', 'xrange', 'zip']
>>>
```

创建
----

```ruby
numbers = [1,2,3]
words = %w[jack rose mike]
```

```python
numbers = [1,2,3]
words = ['jack','rose','mike']
```

长度
----

```ruby
number.size == 3
number.length == 3
number.count == 3
```

```python
len(number) == 3
```


遍历
----

Ruby:

使用Array#each,Array#each\_with\_index和Block
```ruby
  [1,2,3].each{|item| puts item }
  [1,2,3].each_with_index{|item,index| puts index,item }
```

使用for-in语法
```ruby
  for item in [1,2,3] do
    puts item
  end
```

Python:
使用for语法
```python
  for item in [1,2,3]:
    print(item)
```

映射(map)
---------

Ruby:
```ruby
  [1,2,3].map{|item| item * 2} #=> [2,4,6]
```

Python:
使用
[list comprehensions](http://docs.python.org/2/tutorial/datastructures.html#list-comprehensions)
[Python: List Comprehensions](http://www.secnetix.de/olli/Python/list_comprehensions.hawk)

```python
  [item * 2 for item in [1,2,3]] #=> [2,4,6]
```

排序
----

Ruby:
```ruby
[3,2,1].sort # return new sorted array [1,2,3]
[3,2,1].sort! # in place sort [1,2,3]
[2,1,3].sort_by!{|x|-x} # in place sort to [3,2,1]
[2,1,3].sort_by{|x|-x} # retur new array [3,2,1]
```
Python:
sort(...)
    L.sort(cmp=None, key=None, reverse=False) -- stable sort *IN PLACE*;
    cmp(x, y) -> -1, 0, 1
```python
sorted([3,2,1]) # return new sorted array
[3,2,1].sort() # inplace sort

def negate(x,y):
 return y-x
 
[2,1,3].sort(cmp=negate) # inplace sort to [3,2,1]
sorted([2,1,3],cmp=negate) #retur new list [3,2,1]

sorted([2,1,3],cmp=lambda x,y: y-x) #=>[3,2,1]
```

