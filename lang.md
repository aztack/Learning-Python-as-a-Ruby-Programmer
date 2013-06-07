
查看实例类型
------------

Ruby:
```ruby
s = "hello world"
s.class == String
s.is_a? String == true
s.kind_of? String == True
s.is_a? Object == true
s.instance_of? Object = false
s.instance_of? String = true
```
[kind_of? vs. instance_of? vs. is_a?](http://stackoverflow.com/questions/3893278/ruby-kind-of-vs-instance-of-vs-is-a)

Python:
```python
s = "hello world"
s.__class__ == str
isinstance(s,str) == True

import types
types.StringTypes == (str,unicode)
isinstance(s,types.StringTypes) == True
isinstance(s,(str,unicode) == True
isinstance(s,(str,int)) == True
isinstance(s,str) == True
isinstance(s,int) == False
```

[Test if a variable is a list or tuple](http://stackoverflow.com/questions/2184955/test-if-a-variable-is-a-list-or-tuple)

Coercion
--------

Ruby:

[In Ruby, how does coerce() actually work?](http://stackoverflow.com/questions/2799571/in-ruby-how-does-coerce-actually-work)

Python:
