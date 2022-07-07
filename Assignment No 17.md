1. Assign the value 7 to the variable guess_me. Then, write the conditional tests (if, else, and elif) to print the string 'too low' if guess_me is less than 7, 'too high' if greater than 7, and 'just right' if equal to 7.



```python
guess_me = int(input("enter value : "))
if guess_me == 7 :
    print('Just Right')
elif guess_me > 7 :
    print("Too High")
else:
    print('Too Low')
```

    enter value : 7
    Just Right
    


```python

```

 2. Assign the value 7 to the variable guess_me and the value 1 to the variable start. Write a while loop that compares start with guess_me. Print too low if start is less than guess me. If start equals guess_me, print 'found it!' and exit the loop. If start is greater than guess_me, print 'oops' and exit the loop. Increment start at the end of the loop



```python
guess_me = 7
start = 1

while True:
    if start < guess_me:
        print('too low')
    elif start == guess_me:
        print('found it!')
        break
    else:
        print('oops')
        break
    start += 1
```

    too low
    too low
    too low
    too low
    too low
    too low
    found it!
    


```python

```

3. Print the following values of the list [3, 2, 1, 0] using a for loop.



```python
lst = [3,2,1,0]
for i in lst:
    print(i)
```

    3
    2
    1
    0
    


```python

```

4. Use a list comprehension to make a list of the even numbers in range(10)



```python
even = [number for number in range(10) if number % 2 == 0]
```


```python
even
```




    [0, 2, 4, 6, 8]




```python

```

5. Use a dictionary comprehension to create the dictionary squares. Use range(10) to return the keys, and use the square of each key as its value.



```python
squares = {num: num * num for num in range(10)}
```


```python
squares
```




    {0: 0, 1: 1, 2: 4, 3: 9, 4: 16, 5: 25, 6: 36, 7: 49, 8: 64, 9: 81}




```python

```

6. Construct the set odd from the odd numbers in the range using a set comprehension (10).



```python
odd = set(num for num in range(10) if num % 2 == 1)
```


```python
odd
```




    {1, 3, 5, 7, 9}




```python

```

7. Use a generator comprehension to return the string 'Got' and a number for the numbers in range(10). Iterate through this by using a for loop.



```python
string_generator = ('Got ' + str(num) for num in range(10))
for item in string_generator:
    print(item)
```

    Got 0
    Got 1
    Got 2
    Got 3
    Got 4
    Got 5
    Got 6
    Got 7
    Got 8
    Got 9
    


```python

```

8. Define a function called good that returns the list ['Harry', 'Ron', 'Hermione'].



```python
def good():
        return ['Harry', 'Ron', 'Hermione']
```


```python
good()
```




    ['Harry', 'Ron', 'Hermione']




```python

```

9. Define a generator function called get_odds that returns the odd numbers from range(10). Use a for loop to find and print the third value returned.



```python
def get_odds():
    for number in range(1, 10, 2):
         yield number
count = 1
for number in get_odds():
    if count == 3:
        print("The third odd number is", number)
        break
    count += 1  
```

    The third odd number is 5
    


```python

```

10. Define an exception called OopsException. Raise this exception to see what happens. Then writethe code to catch this exception and print 'Caught an oops'



```python
class OopsException(Exception):
        pass
```


```python
 raise OopsException()
```


    ---------------------------------------------------------------------------

    OopsException                             Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_6184/2637122178.py in <module>
    ----> 1 raise OopsException()
    

    OopsException: 



```python
try:
    raise OopsException
except OopsException:
    print('Caught an oops')
```

    Caught an oops
    


```python

```

11. Use zip() to make a dictionary called movies that pairs these lists:

titles = ['Creature of Habit', 'Crewel Fate']

plots = ['A nun turns into a monster', 'A haunted yarn shop'].



```python
titles = ['Creature of Habit', 'Crewel Fate']
plots = ['A nun turns into a monster', 'A haunted yarn shop']
movies = dict(zip(titles, plots))
```


```python
movies
```




    {'Creature of Habit': 'A nun turns into a monster',
     'Crewel Fate': 'A haunted yarn shop'}




```python

```
