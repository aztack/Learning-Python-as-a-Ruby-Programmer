创建
----
Ruby:  
```ruby
 who = '"world"' # 单引号字面量不进行插值，也可以写成 
 #who = %q["world"]
 s = "hello #{who}!" #双引号进行插值，也可以写成
 #s = %Q|hello #{who}!|
 #s = "hello %s!" % who
 #s = sprintf("hello %s!,who)
```

Python:
```python
 exclaimation = "!"
 who = '"world"'
 s = "hello {0}{1}".format(who,exclaimation) #用format方法格式化字符串，也可以写成
 #s = "hello %s%s" % (who,exclaimation)
```

截取子串 
--------

Ruby:
```ruby
  s = "hello world!"
  s[2..3] == "ll"
  s[2...3] == "l"
  s[2..-1] == "llo world!"
  s[2...-1] == "llo world"
  s[2,3] == "llo"
  s["o w"] == "o w"
  s["..."] == nil
  s[/e.*?o/] == "ello"
```

Python:
```python
  s = "hello world!"
  s[2:4] == "ll"
  s[2:3] == "l"
  s[2:] == "llo world!"
  s[2:-1] == "llo world"
  #
  #
  #
  re.compile(r'e.*?o').findall(s) == "ello"
```

转化为数组
----------

```ruby
 s = "hello world!"
 s.split == ["hello","world!"]
 '1 2 3 4'.split(' ',2) == ["1", "2 3 4"]
 'hello'.split('') == ["h", "e", "l", "l", "o"]
```

```python
 s = "hello world!"
 s.split() == ['hello', 'world!']
 '1 2 3 4'.split(' ',2) == ['1', '2', '3 4']
 [c for c in 'hello'] == ['h', 'e', 'l', 'l', 'o']
```

遍历
----
