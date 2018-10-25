### Python Tips

#### download file
```python
# download image from url use urlretrieve
import os
import urllib.request import urlopen
import urllib.request import urlretrieve
from bs4 import BeautifulSoup

html = urlopen("http://www.pythonscraping.com")
bsObj = BeautifulSoup(html, "html.parser")
# image link in the [src] of the html
imageLocation = bsObj.find("a", {"id":"logo"}).find("img")["src"]
# give download link, and second set a file name
urlretrieve(imageLocation, "logo.jpg")

```
#### explore json data
```python
import json

jsonString = '{"arrayOfNums":[{"number": 0}, {"number":1},{"number":2}], \
               "arrayOfFruits":[{"fruits":"apple"}]}'
```

#### python 代码中间换行
- 空格加\