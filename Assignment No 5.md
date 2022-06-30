1. What does an empty dictionary's code look like?

Two curly brackets: {  }


```python

```

2. What is the value of a dictionary value with the key 'foo' and the value 42?


```python
{'foo': 42}
```




    {'foo': 42}




```python

```


3. What is the most significant distinction between a dictionary and a list?

Dictionaries are unordered collection of data points. It uses key, value structure to store the values.

Lists have ordered items


```python

```

4. What happens if you try to access spam['foo'] if spam is {'bar': 100}?


```python
spam= {'bar': 100}
```


```python
spam['foo']
```


    ---------------------------------------------------------------------------

    KeyError                                  Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_17292/3999281786.py in <module>
    ----> 1 spam['foo']
    

    KeyError: 'foo'


here we get a key error


```python

```

5. If a dictionary is stored in spam, what is the difference between the expressions 'cat' in spam and 'cat' in spam.keys()?

There is no difference. The in operator checks whether a value exists as a key in the dictionary.


```python

```

6. If a dictionary is stored in spam, what is the difference between the expressions 'cat' in spam and 'cat' in spam.values()?

'cat' in spam checks if 'cat' key is presend in dictionary or not.

'cat' in spam.values() check 'cat' value in any of the key of spam.


```python
# initialize dictionary
spam = {'dog': 1, 'cat': 2, 'horse': 4}
```


```python
'cat' in spam
```




    True




```python
spam.values()
```




    dict_values([1, 2, 4])




```python
'cat' in spam.values()
```




    False




```python

```

7. What is a shortcut for the following code?

if 'color' not in spam:


   spam['color'] = 'black'


```python
spam = {}
spam.setdefault('color', 'black')
```




    'black'




```python
spam
```




    {'color': 'black'}




```python

```

8. How do you "pretty print" dictionary values using which module and function?

Using pprint.pprint(  ) 

pprint module


```python
import pprint

dict = {'2': 'b', '1': 'a', '3': 'c'}

pprint.pprint(dict)
```

    {'1': 'a', '2': 'b', '3': 'c'}
    


```python

```
