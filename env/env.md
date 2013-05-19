当前运行的脚本路径
------------------
Ruby:
```ruby
puts $0
puts $PROGRAME_NAME
```

Python:
```python
import sys
print(sys.argv[0])
```

当前工作路径
--------

Ruby:
```ruby
Dir.pwd
```

Python:
```python
import os
os.getcwd()
```

如何判断当前脚本是被其他脚本引入或是独立运行
--------------------------------------------

Ruby:
```ruby
if __FILE__ == $0
  #独立运行
else
  #被引用
end
```

Python:
```python
if __name__ == '__main__':
  #独立运行
else:
  #被引用
```
