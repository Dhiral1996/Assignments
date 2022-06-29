1.What are the two values of the Boolean data type? How do you write them?

Answer : True and False are the two values of the boolean data type. We write them as 'T' and 'F'. True and false are not valid booleans and Python will throw an error for them. Internally Python represents True as 1 and False as 0.


```python

```

2. What are the three different types of Boolean operators?

Answer : AND operator ("and") 

   OR operator ("or")
         
   NOT operator ("not") 


```python

```

3. Make a list of each Boolean operator's truth tables (i.e. every possible combination of Boolean
values for the operator and what it evaluate ).

Answer : True and True is True.

True and False is False.

False and True is False.

False and False is False.

True or True is True.

True or False is True.

False or True is True.

False or False is False.

not True is False.

not False is True.


```python

```

4. What are the values of the following expressions?


(5 > 4) and (3 == 5) not (5 > 4) (5 > 4) or (3 == 5) not ((5 > 4) or (3 == 5)) (True and True) and (True == False) (not False) or (not True)


```python
##Answer
(5 > 4) and (3 == 5)
```




    False




```python
not (5 > 4)
```




    False




```python
(5 > 4) or (3 == 5)
```




    True




```python
not ((5 > 4) or (3 == 5))
```




    False




```python
(True and True) and (True == False)
```




    False




```python
(not False) or (not True)
```




    True




```python

```

5. What are the six comparison operators?

Answer :  == ,    != ,    < ,    > ,    <= ,    >=


```python

```

6. How do you tell the difference between the equal to and assignment operators?Describe a
condition and when you would use one.

Answer : 
    
== is the equal to operator that compares two values and evaluates to a Boolean, while = is the assignment operator that stores a value in a variable.

For example:-

x=50   y=100   z=100

(x==y) is False because we assigned different values to x and y.

(y==z) is True because we assign equal values to y and z.

A condition is an expression used in a flow control statement that evaluates to a Boolean value.
    



7. Identify the three blocks in this code:

spam = 0 if spam == 10: print('eggs') if spam > 5: print('bacon') else: print('ham') print('spam') print('spam')



Answer :
    The three blocks are everything inside the if statement and the lines print('bacon') and print('ham').

print('eggs') if spam > 5: print('bacon') else: print('ham') print('spam')


```python

```

8. Write code that prints Hello if 1 is stored in spam, prints Howdy if 2 is stored in spam, and prints Greetings! if anything else is stored in spam.


```python
if spam == 1: 
    print('Hello') 

elif spam == 2:
    print('Howdy') 
    
else: 
    print('Greetings!')
```


```python

```

9.If your programme is stuck in an endless loop, what keys you’ll press?

Answer :  Press CTRL+C to stop a program stuck in an infinite loop.


```python

```

10. How can you tell the difference between break and continue?

Answer :  1)The break statement is primarily used as the exit statement, which helps in escaping from the current block or loop and the continue statement helps in jumping from the current loop iteration to the next loop.

2)whenever break statement executed then else block will not be executed whereas in continue ,all the time else block is executed.


```python

```

11. In a for loop, what is the difference between range(10), range(0, 10), and range(0, 10, 1)?

Answer : They all give the same output. 
    
   The range(10) call ranges from 0 up to 10 but does not include 10
    
   The range(0, 10) tells us that loop to start at 0 up to 10 but does not include 10
    
   The range(0, 10, 1) tells the loop to increase the variable by 1 on each iteration up to 10 but does not include 10
    
    
    


```python

```

12. Write a short program that prints the numbers 1 to 10 using a for loop. Then write an equivalent program that prints the numbers 1 to 10 using a while loop.


```python
for i in range(1, 11):
    print(i)
```

    1
    2
    3
    4
    5
    6
    7
    8
    9
    10
    


```python
i = 1
while i <= 10:
    print(i)
    i = i + 1
```

    1
    2
    3
    4
    5
    6
    7
    8
    9
    10
    


```python

```

13. If you had a function named bacon() inside a module named spam, how would you call it after importing spam?

Answer :  The fucntion can be called with spam.bacon()


```python

```
