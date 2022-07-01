1. What are escape characters, and how do you use them?

Escape characters represent characters in string values that would otherwise be difficult or impossible to type into code. In Python strings, the backslash " \ " is a special character, also called the "escape" character. It is used in representing certain whitespace characters: " \t " is a tab, " \n " is a newline, and " \r " is a carriage return.


```python
print('I'm Pretty Sure 'Exploring' Is Code')
```


      File "C:\Users\dhira\AppData\Local\Temp/ipykernel_20020/3609631579.py", line 1
        print('I'm Pretty Sure 'Exploring' Is Code')
                 ^
    SyntaxError: invalid syntax
    



```python
print('I\'m Pretty Sure \'Exploring\' Is Code')
```

    I'm Pretty Sure 'Exploring' Is Code
    


```python

```

2. What do the escape characters n and t stand for?

\n is a newline; \t is a tab.


```python
# Use of \n
print("Hello!!!\nI'm in Mumbai.")
```

    Hello!!!
    I'm in Mumbai.
    


```python
# Use of \t
print("Hello!!!\tI'm Banglore.")
```

    Hello!!!	I'm Banglore.
    


```python

```

3. What is the way to include backslash characters in a string?

A blackslash character can be introduced with double blackslash characters.


```python
# Using single backslash character
print('\')
```


      File "C:\Users\dhira\AppData\Local\Temp/ipykernel_20020/1254780951.py", line 2
        print('\')
                  ^
    SyntaxError: EOL while scanning string literal
    



```python
print('\\')
```

    \
    


```python

```

4. The string "Howl's Moving Castle" is a correct value. Why isn't the single quote character in the word Howl's not escaped a problem?

The single quote in Howl's is fine because we have used double quotes to mark the beginning and end of the string.


```python

```

5. How do you write a string of newlines if you don't want to use the n character?

By default print statements add a new line character at the end of the string. We have to use multiline approach.


```python
print("Hello")
print("World")
```

    Hello
    World
    


```python

```

6. What are the values of the given expressions?

'Hello, world!'[1] 

'Hello, world!'[0:5] 

'Hello, world!'[:5] 

'Hello, world!'[3:]


```python
'Hello, world!'[1] 
```




    'e'




```python
'Hello, world!'[0:5] 
```




    'Hello'




```python
'Hello, world!'[:5] 
```




    'Hello'




```python
'Hello, world!'[3:]
```




    'lo, world!'




```python

```

7. What are the values of the following expressions?

'Hello'.upper() 

'Hello'.upper().isupper() 

'Hello'.upper().lower()


```python
'Hello'.upper()
```




    'HELLO'




```python
'Hello'.upper().isupper()
```




    True




```python
'Hello'.upper().lower()
```




    'hello'




```python

```

8. What are the values of the following expressions?

'Remember, remember, the fifth of July.'.split() '-'.join('There can only one.'.split())




```python
'Remember, remember, the fifth of July.'.split()
```




    ['Remember,', 'remember,', 'the', 'fifth', 'of', 'July.']




```python
'-'.join('There can only one.'.split())
```




    'There-can-only-one.'




```python

```

9. What are the methods for right-justifying, left-justifying, and centering a string?|

The rjust(), ljust(), and center() string methods, respectively


```python
s = "hello"
length = 10
fillchars = "$"

print(s.rjust(length, fillchars))
```

    $$$$$hello
    


```python
s = "hello"
length = 10
fillchars = "$"

print(s.ljust(length, fillchars))
```

    hello$$$$$
    


```python
s = "hello"
length = 10
fillchars = "$"

print(s.center(length, fillchars))
```

    $$hello$$$
    


```python

```

10. What is the best way to remove whitespace characters from the start or end?

The lstrip() and rstrip() methods remove whitespace from the left and right ends of a string, respectively.


```python

```
