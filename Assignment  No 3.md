1. Why are functions advantageous to have in your programs?

Functions reduces the need for duplicate code. This makes programs shorter, easier to read, and easier to update.


```python

```

2. When does the code in a function run: when it's specified or when it's called?

The code in a function executes when the function is called, not when the function is defined.


```python

```

3. What statement creates a function?

The def statement defines and creates a function.


```python

```

4. What is the difference between a function and a function call?

A function is a block of code that does a particular operation and returns a result. It usually accepts inputs as parameters and returns a result.A function consists of the def statement and the code in its def clause.


A function call is what moves the program execution into the function, and the function call evaluates to the function’s return value.

5. How many global scopes are there in a Python program? How many local scopes?

One global scope and a local scope is created whenever a function is called.
The global scope is created once the program starts and gets destroyed with the termination of the python program.
The local scope in a python program is defined for a block of code such as function. Each function in a python program has its own local scope in which all its variables  and object names are defined. 


```python

```

6. What happens to variables in a local scope when the function call returns?

When a function call returns, the local scope is destroyed, and all the variables in it are forgotten.


```python

```

7. What is the concept of a return value? Is it possible to have a return value in an expression?

The specific value returned from a function is called the return value. Like any value, a return value can be used as part of an expression.


```python

```

8. If a function does not have a return statement, what is the return value of a call to that function?

If there is no return statement for a function, its return value is None.


```python

```

9. How do you make a function variable refer to the global variable?

A global statement will force a variable in a function to refer to the global variable. Hence using global statement we can make function variable refer to global variable.


```python

```

10. What is the data type of None?

The data type of None is NoneType.


```python

```

11. What does the sentence import areallyourpetsnamederic do?

This import statement imports a module named areallyourpetsnamederic.


```python

```

12. If you had a bacon() feature in a spam module, what would you call it after importing spam?

This function can be called with spam.bacon().


```python

```

13. What can you do to save a programme from crashing if it encounters an error?

Place the line of code that might cause an error in a try and except clause 



14. What is the purpose of the try clause? What is the purpose of the except clause?

The code that could potentially cause an error goes in the try clause.


The code that executes if an error happens goes in the except clause.


First, try clause is executed it means the code between try and except clause. If there is no exception, then only try clause will run, except clause is finished. If any exception occured, try clause will be skipped and except clause will run.


```python

```
