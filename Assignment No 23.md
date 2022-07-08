1. What is the result of the code, and why?


def func(a, b=6, c=8):

    print(a, b, c)
    
func(1, 2)

Here as we have hardcoded and sent 2 values therefore preference is given to the input user gives. so a=1,b=2,c as by default argument 8.


```python
def func(a, b=6, c=8):
    print(a, b, c)
func(1, 2)
```

    1 2 8
    


```python

```

2. What is the result of this code, and why?


def func(a, b, c=5):

    print(a, b, c)
    
func(1, c=3, b=2)

here a=1,b=2(hardcoded by user),c=3(hardcoded by user). position doesnt matter as long as we have mentioned the variable to which value is assigned.




```python
def func(a, b, c=5):
    print(a, b, c)
func(1, c=3, b=2)
```

    1 2 3
    


```python

```

3. How about this code: what is its result, and why?


def func(a, *pargs):
    
    print(a, pargs)
    
func(1, 2, 3)

Here a=1. *pargs returns as many argument user gives as input in form of tuples


```python
def func(a, *pargs):
    print(a, pargs)
func(1, 2, 3)
```

    1 (2, 3)
    


```python

```

4. What does this code print, and why?


def func(a, **kargs):
    
    print(a, kargs)
    
func(a=1, c=3, b=2)

Here a=1. **kargs returns as many argument user gives as input in form of dictionary


```python
def func(a, **kargs):
    print(a, kargs)
func(a=1, c=3, b=2)
```

    1 {'c': 3, 'b': 2}
    


```python

```

5. What gets printed by this, and explain?


def func(a, b, c=8, d=5): 
    
    print(a, b, c, d)
    
func(1, *(5, 6))

   '*'  is the unpacking operator and are operators that unpack the values from iterable objects in Python. The single 
    asterisk operator * can be used on any iterable that Python provides, while the double asterisk operator ** can only 
    be used on dictionaries. In the example the value *(5,6) will be unpacked and will be assigned to b and c and passed 
    as arguments, d =5 will taken by defaults are keyword arguments.


```python
def func(a, b, c=8, d=5): 
    print(a, b, c, d)
func(1, *(5, 6))
```

    1 5 6 5
    


```python

```

6. what is the result of this, and explain?

def func(a, b, c): 
    
    a = 2; b[0] = 'x'; c['a'] = 'y'

l=1; m=[1]; n={'a':0}

print(l,m,n)

func(l, m, n)

l, m, n

Here in func(l,m,n) we passed l=1(user input), m is passed as list contain 1 element i.e 'x', n is passed as dictionary i.e {'a':'y'}


```python
def func(a, b, c): 
    a = 2; b[0] = 'x'; c['a'] = 'y'
    
l=1; m=[1]; n={'a':0}

func(l, m, n)
l, m, n
```




    (1, ['x'], {'a': 'y'})




```python

```
