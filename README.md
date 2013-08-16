给Ruby程序员的Python学习小册(Learning Python as a Ruby Programmer)
==================================================================

设计哲学
--------
Ruby:
> Matsumoto has said that Ruby is designed for programmer productivity and fun, following the principles of good user interface design.[27] He stresses that systems design needs to emphasize human, rather than computer, needs

[Ruby设计哲学](http://en.wikipedia.org/wiki/Ruby_\(programming_language\))

Python:

体会Python的设计与Ruby的不同。使用Python时Be Pythonic，使用Ruby时Go The Ruby Way。
在比较中你会发现，完成一个功能时，Ruby有很多方法可以选择。有的方法还有别名。而Python中，大多数情况下只有一种’显而易见‘的实现方式。

```python
>>> import this
The Zen of Python, by Tim Peters

**Beautiful** is better than ugly.
**Explicit** is better than implicit.
**Simple** is better than complex.
**Complex** is better than complicated.
**Flat** is better than nested.
**Sparse** is better than dense.
**Readability** counts.
Special cases aren't special enough to break the rules.
Although **practicality** beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, **refuse the temptation to guess**.

**There should be one-- and preferably only one --obvious way to do it**.

Although that way may not be obvious at first unless you're Dutch.
**Now** is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```

查看可用函数 
------------

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

[Python Built-in Functions](http://docs.python.org/2.7/library/functions.html)

自动完成
--------

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

[设置参考](http://www.razorvine.net/blog/user/irmen/article/2004-11-22/17)

Update: 10:48 2013/5/24
-----------------------
推荐Ruby和Python的两个支持自动完成、代码高亮的Shell:

- [Pry is a powerful alternative to the standard IRB shell for Ruby.](https://github.com/pry/pry)
- [bpython is a fancy interface to the Python interpreter for Linux, BSD, OS X and Windows](http://www.bpython-interpreter.org/)
- 

Update: 11:00 2013/08/16
------------------------
[Interpreted Languages: Perl, PHP, Python, Ruby (Sheet One)
a side-by-side reference sheet](http://hyperpolyglot.org/scripting)
