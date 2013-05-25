
遍历文本文件中每一行

```ruby
File.readlines('a.txt').each do |line|
  # ...
end
```

```python
with open('a.txt') as file:
  for line in file.readlines():
    # ...
```
