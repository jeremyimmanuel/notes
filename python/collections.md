# Collections

Collections library from python standard library
For official docs click [here](https://docs.python.org/3.8/library/collections.html)

## defaultdict

Implements default value if code calls non-exisiting key

```py
from collections import defaultdict as dd

d = dd(lambda : 0) # default value would be 0
d['a'] # -> will return 0
```

## Counter

Takes in an iterable and counts the instances of each element.
Inherites defaultdicts' behavior of having a default value of 0.

```py
from collections import Counter
c = Counter('Jeremy')
c['e'] # -> will return 2 because there's two instances of 'e' in 'Jeremy'
```

## OrderedDict

Dict subclass that remembers the order entries were added

```py
from collections import OrderedDict

```
