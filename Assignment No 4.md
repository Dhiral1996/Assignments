1. What exactly is [   ]?

The empty list value, which is a list value that contains no items. This is similar to how '  ' is the empty string value.


```python

```

2. In a list of values stored in a variable called spam, how would you assign the value 'hello' as the third value?

Lets assume [2,4,6,8,10] are in spam 


```python
spam =[2,4,6,8,10]
```


```python
spam[2] = 'hello'
```


```python
spam
```




    [2, 4, 'hello', 8, 10]




```python

```

Let's pretend the spam includes the list ['a', 'b', 'c', 'd'] for the next three queries.


```python
spam=['a', 'b', 'c', 'd']
```


```python

```

3. What is the value of spam[int(int('3' * 2) / 11)]?


```python
spam[int(int('3' * 2) / 11)]
```




    'd'




```python

```

4. What is the value of spam[-1]?


```python
spam[-1]
```




    'd'




```python

```

5. What is the value of spam[:2]?


```python
spam[:2]
```




    ['a', 'b']




```python

```

Let's pretend bacon has the list [3.14, 'cat,' 11, 'cat,' True] for the next three questions.


```python
bacon=[3.14, 'cat', 11, 'cat', True]
```


```python

```

6. What is the value of bacon.index('cat')?


```python
bacon.index('cat')
```




    1




```python

```

7. How does bacon.append(99) change the look of the list value in bacon?


```python
bacon.append(99)
```


```python
bacon
```




    [3.14, 'cat', 11, 'cat', True, 99]




```python

```

8. How does bacon.remove('cat') change the look of the list in bacon?


```python
bacon.remove('cat')
```


```python
bacon
```




    [3.14, 11, 'cat', True, 99]




```python

```

9. What are the list concatenation and list replication operators?

The operator for list concatenation is +, while the operator for replication is *.


```python

```

10. What is difference between the list methods append() and insert()?

 Here append( ) will add values only to the end of a list, insert( ) can add them anywhere in the list.


```python

```

11. What are the two methods for removing items from a list?

The del statement and the remove( ) list method are two ways to remove values from a list.


```python

```

12. Describe how list values and string values are identical.

Here both lists and strings can be passed to len( ), they have indexes and slices,can be used in for loops, can be concatenated or replicated, and can be used with the in and not in operators.


```python

```

13. What's the difference between tuples and lists?

Lists are mutable so they can have values added, removed, or changed. Tuples are immutable so they cannot be changed at all. Also, tuples are written using parentheses, (  ), while lists use the square brackets, [  ].


```python

```

14. How do you type a tuple value that only contains the integer 42?


```python
my_tuple = (42,)
my_tuple, type(my_tuple)
```




    ((42,), tuple)




```python

```

15. How do you get a list value's tuple form? How do you get a tuple value's list form?

Using the tuple() and list() functions, respectively


```python
my_list = [1,2,3,4]
print(tuple(my_list))
```

    (1, 2, 3, 4)
    


```python
my_tuple = (1,2,3,4)
print(list(my_tuple))
```

    [1, 2, 3, 4]
    


```python

```

16. Variables that "contain" list values are not necessarily lists themselves. Instead, what do they contain?

Variables do not store values directly.

Python variables work with references to objects representing the values.

For example, we have

a = [1,2,3]

Python creates a new reference for a to point at the object representing the value [1,2,3] in the memory.


```python

```

17. How do you distinguish between copy.copy() and copy.deepcopy()?

The copy.copy() function will do a shallow copy of a list, while the copy.deepcopy() function will do a deep copy of a list. That is, only copy.deepcopy() will duplicate any lists inside the list.

Let's understand by an example,


```python
# import copy module
import copy

# initialize our list
my_list = [1, [2, 3], 4]
```


```python
copy_list = copy.copy(my_list)
#copy_list becomes new object but my_list[1] is same object as copy_list[1
print(id(my_list))
print(id(copy_list))

print(id(my_list[1]))
print(id(copy_list[1]))
```

    2679580535232
    2679558367936
    2679580335168
    2679580335168
    


```python

```


```python
deepcopy_list = copy.deepcopy(my_list)
deepcopy_list becomes new object and my_list[1] is new object
print(id(my_list))
print(id(deepcopy_list))

print(id(my_list[1]))
print(id(deepcopy_list[1]))
```

    2679580535232
    2679580255360
    2679580335168
    2679580448000
    


```python

```
