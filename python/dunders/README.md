# Dunder Methods

In python, there are a handful of implicit functions that are represented with a double underscore between the function.

## __init__

Object/class initializier

```py
def __init__(self, a, b):
    self.a = a
    self.b = b
```

## __call__

Makes the object behave like a function.

```py
class A:
    def __call__(self, n: int):
        # some code

test = A()
test(5)

```