1. What is the result of the code, and explain?

X = 'iNeuron'

def func():

    print(X)
    
func()

The global variables are accessible inside the functions in python. But we can not access function variable out side 
function. 
Since x is golbal variable we are able to print it in side the function
solution : 'iNeuron'


```python
X = 'iNeuron'
def func():
    print(X)
    
func()
```

    iNeuron
    


```python

```

2. What is the result of the code, and explain?


X = 'iNeuron'

def func():
    
    X = 'NI!'

func()

print(X)

Here when func() is called it will execute the statement written inside it which only initialize value of x='NI' but it doesnot return anything(None).So it comes out of the block and doesnot print anything. Again when print(x) is executed it prints the value of X = 'iNeuron'.


```python
X = 'iNeuron'
def func():
    X = 'NI!'

func()
print(X)
```

    iNeuron
    


```python

```

3. What does this code print, and why?


X = 'iNeuron'

def func():
    
    X = 'NI!'
    
    print(X)

func()

print(X)

The global variables are access in side the functions in python. But we can not access function variable out side 
function. X is updated with 'NI' which is local to function and its immutable. its name space is with in the function
solution = 'NI!', 'iNeuron'


```python
X = 'iNeuron'
def func():
    X = 'NI!'
    print(X)

func()
print(X)
```

    NI!
    iNeuron
    


```python

```

4. What output does this code produce? Why?


X = 'iNeuron'

def func():
    
    global X
    
    X = 'NI!'
    
    print(X)

func()

print(X)


 since the X in side function is made Global, it will be accesible out side of the function too. now X will have new value.

 solution : 'NI!', 'NI!'


```python
X = 'iNeuron'
def func():
    global X
    X = 'NI!'
    print(X)

func()
print(X)
```

    NI!
    NI!
    


```python

```

5. What about this code—what’s the output, and why?


X = 'iNeuron'

def func():

    X = 'NI'
    
def nested():

    print(X)

nested()

func()

X


the nested() function will print 'iNeuron', Then func() does not display anything, and x ='NI' is not accessible out 
side the function.
Solution : 'iNeuron'


```python
X = 'iNeuron'
def func():
    X = 'NI'
def nested():
    print(X)
    
nested()
func()
X
```

    iNeuron
    




    'iNeuron'




```python

```

6. How about this code: what is its output in Python 3, and explain?


X = 'kkl'

def func():
    
    X = 'NI'
    
    def nested():
        
        nonlocal X
        
        X = 'spam'
        
    nested()
    
    print(X)
    
 func()

Nonlocal variables are used in nested functions whose local scope is not defined. 
This means that the variable can be neither in the local nor the global scope. it print the updated value from nested 
function

Solution : 'spam'


```python
def func():
    X = 'NI'
    def nested():
        nonlocal X
        X = 'spam'
    nested()
    print(X)

func()
```

    spam
    


```python

```
