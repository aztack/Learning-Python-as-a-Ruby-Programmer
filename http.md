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
open("http://www.google.com") do |file| ##<File:d:/tmp/other/open-uri20130607-13872-1c2fm1l>, Tempfile
  html = file.read
  #...
end
```

Python:
```python
import urllib
addinforurl = urllib.urlopen("http://www.google.com") #<class urllib.addinfourl at ...>
html = addinforurl.read()
```

