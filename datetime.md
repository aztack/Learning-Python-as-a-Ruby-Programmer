得到当前日期、时间及格式化
--------------------------

Ruby:

```ruby
> Time.now
=> 2013-06-07 17:43:59 +0800
> Date.today
=> #<Date: 2013-06-07 ((2456451j,0s,0n),+0s,2299161j)>
> Date.today.to_s
=> "2013-06-07"
> Time.now.strftime "%Y/%m/%d %H:%M:%S"
=> "2013/06/07 17:45:58"
```

Python:

```python
>>> import time
>>> time.strftime("%Y/%m/%d %H:%M:%S",time.localtime())
'2013/06/07 18:00:26'
```
