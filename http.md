HTTP
====

获取页面

Ruby:

```ruby
require 'net/http'
url = "http://www.google.com"
html = Net::HTTP.get(URI.parse(url))
#...
```

或者使用`open-uri`
```ruby
require 'open-uri'
open("http://www.google.com") do |file|
  html = file.read
  #...
end
```

Python:
```python
import urllib
html = urllib.urlopen("http://www.google.com").read()
```

