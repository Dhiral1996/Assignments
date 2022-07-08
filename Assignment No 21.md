1. Add the current date to the text file today.txt as a string.



```python
import datetime
from datetime import date
now = date.today()
cur_date = now.isoformat()
cur_date
```




    '2022-07-08'




```python
with open('today.txt','w') as file:
    file.write(cur_date)
```


```python

```

2. Read the text file today.txt into the string today_string



```python
with open('today.txt','r') as file:
    today_string = file.read()
today_string
```




    '2022-07-08'




```python

```

3. Parse the date from today_string.



```python
from datetime import datetime
format = '%Y-%m-%d'
datetime.strptime(today_string,format)
```




    datetime.datetime(2022, 7, 8, 0, 0)




```python

```

4. List the files in your current directory



```python
import os
os.listdir('.')
```




    ['-1.14-windows.xml',
     '.astropy',
     '.bash_history',
     '.conda',
     '.condarc',
     '.continuum',
     '.cufflinks',
     '.docker',
     '.idlerc',
     '.ipynb_checkpoints',
     '.ipython',
     '.jupyter',
     '.lesshst',
     '.matplotlib',
     '.vscode',
     'addresses.csv',
     'airfoil_self_noise.dat',
     'anaconda3',
     'AppData',
     'Application Data',
     'Assignment  No 3.ipynb',
     'Assignment 1 .ipynb',
     'Assignment No 1.ipynb',
     'Assignment No 10.ipynb',
     'Assignment No 11.ipynb',
     'Assignment No 12.ipynb',
     'Assignment No 13.ipynb',
     'Assignment No 14.ipynb',
     'Assignment No 15.ipynb',
     'Assignment No 16.ipynb',
     'Assignment No 17.ipynb',
     'Assignment No 19.ipynb',
     'Assignment No 2.ipynb',
     'Assignment No 20.ipynb',
     'Assignment No 21.ipynb',
     'Assignment No 4.ipynb',
     'Assignment No 5.ipynb',
     'Assignment No 6.ipynb',
     'Assignment No 7.ipynb',
     'Assignment No 8.ipynb',
     'Assignment No 9.ipynb',
     'bank.csv',
     'batman.png',
     'batman1.gif',
     'books.csv',
     'books.db',
     'Contacts',
     'Cookies',
     'cricket.csv',
     'Customers.csv',
     'Decisiontree.ipynb',
     'Desktop',
     'Documents',
     'Downloads',
     'example.tsv',
     'example.txt',
     'Favorites',
     'FlightPrediction.ipynb',
     'for loops while loop.ipynb',
     'glass.data',
     'Graph.ipynb',
     'graphs day 2.ipynb',
     'GUI Programming-1.ipynb',
     'Hierarichal Means.ipynb',
     'Hypothesis_Testing.ipynb',
     'if else , for loop.ipynb',
     'ineuron.db',
     'IntelGraphicsProfiles',
     'iron-man-tony-stark.gif',
     'jobdb.db',
     'json_res.csv',
     'K MEans Clustering.ipynb',
     'K Nearest Neighbors with Python.ipynb',
     'Lassoand Regression.ipynb',
     'Links',
     'Local Settings',
     'Logisstic Practical.ipynb',
     'LUSID Excel - Business Agility - Making Simple Changes Quickly & Easily.xlsx',
     'LUSID Excel - Maintain a product in multiple currencies and share classes.xlsx',
     'LUSID Excel - Manage instruments with economic definitions.xlsx',
     'LUSID Excel - Manage Orders.xlsx',
     'LUSID Excel - Manage your investment strategies.xlsx',
     'LUSID Excel - Setting up your IBOR.xlsx',
     'LUSID Excel - Setting up your market data.xlsx',
     'model.pkl',
     'Music',
     'My Documents',
     'nba.csv',
     'NetHood',
     'not working.ipynb',
     'NTUSER.DAT',
     'ntuser.dat.LOG1',
     'ntuser.dat.LOG2',
     'NTUSER.DAT{bb6ab8be-56b3-11ec-b454-9843fa72f7ee}.TM.blf',
     'NTUSER.DAT{bb6ab8be-56b3-11ec-b454-9843fa72f7ee}.TMContainer00000000000000000001.regtrans-ms',
     'NTUSER.DAT{bb6ab8be-56b3-11ec-b454-9843fa72f7ee}.TMContainer00000000000000000002.regtrans-ms',
     'ntuser.ini',
     'numpy day 2.ipynb',
     'OneDrive',
     'oops 29th .ipynb',
     'oops 30th.ipynb',
     'oops class 1.ipynb',
     'pandas .ipynb',
     'pandas and numpy.ipynb',
     'pandas class 3.ipynb',
     'pandas day 2.ipynb',
     'person.db',
     'Placement Assignment .ipynb',
     'Postman',
     'Practise Problems (1).ipynb',
     'PrintHood',
     'Project',
     'PycharmProjects',
     'Python basic (3).ipynb',
     'Recent',
     'review scrapper.ipynb',
     'sample_submission.csv',
     'Saved Games',
     'scraper.py',
     'seaborn-data',
     'Searches',
     'SendTo',
     'Silhoutte Scoring.ipynb',
     'Start Menu',
     'SVM Kernelss Implementation.ipynb',
     'Templates',
     'test.csv',
     'test.txt',
     'today.txt',
     'train.csv',
     'Tuples , set , dict .ipynb',
     'Untitled.ipynb',
     'Untitled1.ipynb',
     'Untitled10.ipynb',
     'Untitled11.ipynb',
     'Untitled12.ipynb',
     'Untitled13.ipynb',
     'Untitled14.ipynb',
     'Untitled15.ipynb',
     'Untitled16.ipynb',
     'Untitled17.ipynb',
     'Untitled18.ipynb',
     'Untitled19.ipynb',
     'Untitled2.ipynb',
     'Untitled20.ipynb',
     'Untitled21.ipynb',
     'Untitled22.ipynb',
     'Untitled23.ipynb',
     'Untitled24.ipynb',
     'Untitled25.ipynb',
     'Untitled26.ipynb',
     'Untitled27.ipynb',
     'Untitled28.ipynb',
     'Untitled29.ipynb',
     'Untitled3.ipynb',
     'Untitled30.ipynb',
     'Untitled31.ipynb',
     'Untitled32.ipynb',
     'Untitled33.ipynb',
     'Untitled34.ipynb',
     'Untitled35.ipynb',
     'Untitled36.ipynb',
     'Untitled37.ipynb',
     'Untitled38.ipynb',
     'Untitled39.ipynb',
     'Untitled4.ipynb',
     'Untitled40.ipynb',
     'Untitled41.ipynb',
     'Untitled42.ipynb',
     'Untitled43.ipynb',
     'Untitled44.ipynb',
     'Untitled45.ipynb',
     'Untitled46.ipynb',
     'Untitled47.ipynb',
     'Untitled48.ipynb',
     'Untitled49.ipynb',
     'Untitled5.ipynb',
     'Untitled50.ipynb',
     'Untitled51.ipynb',
     'Untitled52.ipynb',
     'Untitled6.ipynb',
     'Untitled7.ipynb',
     'Untitled8.ipynb',
     'Untitled9.ipynb',
     'Videos']




```python

```

5. Create a list of all of the files in your parent directory (minimum five files should be available).



```python
import os
os.listdir('..')

```




    ['All Users', 'Default', 'Default User', 'desktop.ini', 'dhira', 'Public']




```python

```

6. Use multiprocessing to create three separate processes. Make each one wait a random number of seconds between one and five, print the current time, and then exit.



```python
import multiprocessing

def printsec(seconds):
    from datetime import datetime
    from time import sleep
    sleep(seconds)
    print('wait', seconds, 'seconds, time is', datetime.utcnow())
    
if __name__ == '__main__':
    import random    
    for n in range(3):
        seconds = random.random()
        proc = multiprocessing.Process(target=printsec, args=(seconds,))
        proc.start()
```


```python

```

7. Create a date object of your day of birth.



```python
my_date = date(1996,8,24)
my_date
```




    datetime.date(1996, 8, 24)




```python

```

8. What day of the week was your day of birth?



```python
my_date.weekday()
```




    5




```python

```

9. When will you be (or when were you) 10,000 days old?



```python
from datetime import timedelta
day10000 = my_date + timedelta(days=10000)
```


```python
day10000
```




    datetime.date(2024, 1, 10)




```python

```
