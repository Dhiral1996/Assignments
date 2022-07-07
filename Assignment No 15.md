1.How many seconds are in an hour? Use the interactive interpreter as a calculator and multiply the number of seconds in a minute (60) by the number of minutes in an hour (also 60).



```python
60*60
```




    3600




```python

```

2. Assign the result from the previous task (seconds in an hour) to a variable called seconds_per_hour.



```python
seconds_per_hour= 60 * 60
seconds_per_hour
```




    3600




```python

```

3. How many seconds do you think there are in a day? Make use of the variables seconds per hour and minutes per hour.



```python
one_day  = 24
second_in_a_day = 24 * seconds_per_hour
second_in_a_day
```




    86400




```python

```

4. Calculate seconds per day again, but this time save the result in a variable called seconds_per_day



```python
seconds_per_day =  24 * seconds_per_hour
seconds_per_day 
```




    86400




```python

```

5. Divide seconds_per_day by seconds_per_hour. Use floating-point (/) division.



```python
seconds_per_day/seconds_per_hour
```




    24.0




```python

```

6. Divide seconds_per_day by seconds_per_hour, using integer (//) division. Did this number agree with the floating-point value from the previous question, aside from the final .0?


Yes


```python
seconds_per_day // seconds_per_hour
```




    24




```python

```

7. Write a generator, genPrimes, that returns the sequence of prime numbers on successive calls to its next() method: 2, 3, 5, 7, 11, ...



```python
def genPrimes():
    primes = []
    n = 2
    last = n

    while True:
        for i in primes:
            if n % i == 0:
                n += 1
                break

        else:
            primes.append(n)
            last = n
            n += 1
            yield last
```


```python
genPrimes()
```




    <generator object genPrimes at 0x000001653C1012E0>




```python
None
def genPrimes():
    primes = [2]
    yield primes[0]
    guess = 3
    while True:
        if all(guess%x != 0 for x in primes):
            primes.append(guess)        
        if guess == primes[-1]:
            yield primes[-1]
        guess += 2
```


```python
genPrimes()
```




    <generator object genPrimes at 0x000001653C101270>




```python

```
