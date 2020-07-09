# Collections

Collections library from python standard library
For official docs click [here](https://docs.python.org/3.8/library/collections.html)

## defaultdict

Implements default value if code calls non-exisiting key
[another](../iOS/Swift/cocoapods.md)
```py
from collections import defaultdict as dd

d = dd(lambda : 0) # default value would be 0
d['a'] # -> would return 0
```

## counter
