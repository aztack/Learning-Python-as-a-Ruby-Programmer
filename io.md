遍历文本文件中每一行
==================

Ruby:
```ruby
File.readlines('a.txt').each do |line|
  # ...
end
```

Python:
```python
with open('a.txt') as file:
  for line in file.readlines():
    # ...
```

```python
file = open('a.txt')
for line in file.readlines():
  #...
file.close()
```

写文件
=====
Ruby:
```ruby
File.write("a.txt","hello!")

File.open("a.txt","w") do |file|
    file.write("hello")
    file.puts("!")
end

File.write("a.txt", (1..10).to_a.join($\))
```

Python:
```python
with open("a.txt","w") as file:file.write("hello!" + os.linesep)

with open("a.txt","w") as file: 
    file.write("hello")
    file.write("!" + os.linesep)

with open("a.txt","w") as file:
    file.write(os.linesep.join(str(n) for n in range(0,10)))
```
