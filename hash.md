Python中对应哈希表的数据结构叫dict

创建哈希表
----------

Ruby:
Ruby中的key多用symbol
```ruby
#字面量
h = {:name:'jack',age:20}
Hash[1,2,3,4] #=> {[1, 2]=>[3, 4]}
puts h[:name]
```

Python:
Python中，哈希表的key必须是immutable的，比如字符串。
```python
h = {'name':'jack','age':20}
print(h['name'])
```

移除名值对
----------

Ruby:
```ruby
h.delete(:name) == 'jack'
h.delete_if{|k,v| k == :name}
```

Python:
```python
del h['name']
```


遍历哈希表
----------

Ruby:
```ruby
for k,v in h do
#
end

h.each{|k,v| ... }
h.each_with_index{|kv,i| ... }
h.each_with_index{|(k,v),i| ... }
h.each_cons
h.each_slice
h.each_key
h.each_value
```

Python:
```python
for k,v in h.items():
  print("{0}=>{1}".format(k,v))
```
