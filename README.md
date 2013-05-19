Learning-Python-as-a-Ruby-Programmer
====================================

Cookbook of learning Python as a Ruby programmer

在ruby的irb中可以方便的查询类/模块的方法：

```ruby
irb(main):013:0> String.instance_methods(false)
=> [:<=>, :==, :===, :eql?, :hash, :casecmp, :+, :*, :%, :[], :[]=, :insert, :length, :size, :bytesize, :empty?, :=~, :m
atch, :succ, :succ!, :next, :next!, :upto, :index, :rindex, :replace, :clear, :chr, :getbyte, :setbyte, :byteslice, :to_
i, :to_f, :to_s, :to_str, :inspect, :dump, :upcase, :downcase, :capitalize, :swapcase, :upcase!, :downcase!, :capitalize
!, :swapcase!, :hex, :oct, :split, :lines, :bytes, :chars, :codepoints, :reverse, :reverse!, :concat, :<<, :prepend, :cr
ypt, :intern, :to_sym, :ord, :include?, :start_with?, :end_with?, :scan, :ljust, :rjust, :center, :sub, :gsub, :chop, :c
homp, :strip, :lstrip, :rstrip, :sub!, :gsub!, :chop!, :chomp!, :strip!, :lstrip!, :rstrip!, :tr, :tr_s, :delete, :squee
ze, :count, :tr!, :tr_s!, :delete!, :squeeze!, :each_line, :each_byte, :each_char, :each_codepoint, :sum, :slice, :slice
!, :partition, :rpartition, :encoding, :force_encoding, :valid_encoding?, :ascii_only?, :unpack, :encode, :encode!, :to_
r, :to_c]
```

类/模块的继承/包含关系：
```ruby
irb(main):014:0> String.ancestors
=> [String, Comparable, Object, PP::ObjectMixin, Kernel, BasicObject]
```

Python的Interactive Shell中也有类似的方法：

列出
```python
>>> help
Type help() for interactive help, or help(object) for help about object.

>>> help(dir)
Help on built-in function dir in module __builtin__:

dir(...)
    dir([object]) -> list of strings

    If called without an argument, return the names in the current scope.
    Else, return an alphabetized list of names comprising (some of) the attributes
    of the given object, and of attributes reachable from it.
    If the object supplies a method named __dir__, it will be used; otherwise
    the default dir() logic is used and returns:
      for a module object: the module's attributes.
      for a class object:  its attributes, and recursively the attributes
        of its bases.
      for any other object: its attributes, its class's attributes, and
        recursively the attributes of its class's base classes.

>>> dir()
['__builtins__', '__doc__', '__name__', '__package__']
```

在IRB中启用TAB自动完成：
```ruby
require 'irb/completion'
```
如果觉得而每次都敲很麻烦，可以将上面这段代码写到`ruby1.x.x\bin\irb`中。

Python启用TAB自动完成：

``` python
import readline,rlcompleter
readline.parse_and_bind('tab:complete')
```

同样，你可以设置系统环境变量`set PYTHONSTARTUP=c:\users\administrator\.pythonrc`
然后在对应的.pythonrc中写入上面的代码。这样就不用每次都输入了

[参考](http://www.razorvine.net/blog/user/irmen/article/2004-11-22/17)
