# Python: Parameter passed by value or by reference?

### What is pass by value (with eg)

### What is pass by refernce (with eg)

Turns out, Python follows neither of the above. Python is "Pass by object reference" a.k.a object references are passed by value

### What is pass by object reference (with eg)

Now put anomaly example here

```python
import foobar

def foo(x):
    print(x, id(x))
    x +=10
    print(x, id(x))
    return x
    
a =10
print(a, id(a))
b = foo(a)
print(a, id(a)); print(b, id(b))

#why is the change in value not reflected in 'a'?
```

Well, it turns out that the variable 'a'/'x' was still passed by object reference. But since it is of type int (which is immutable); when it is changes the variable is assigned to a new memory location hence the change is not reflected outside the function

### what are mutable and immutable objects in Python?


### what is shallow copy and deep copy?