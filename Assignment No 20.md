1. Set the variable test1 to the string 'This is a test of the emergency text system,' and save test1 to a file named test.txt.



```python
test1 = 'This is a test of the emergency text system'
```


```python
len(test1)
```




    43




```python
outfile = open('test.txt', 'wt')
```


```python
outfile.write(test1)
```




    43




```python
outfile.close()
```


```python

```

2. Read the contents of the file test.txt into the variable test2. Is there a difference between test 1 and test 2?



```python
with open('test.txt', 'rt') as infile:
    test2 = infile.read()
```


```python
test2
```




    'This is a test of the emergency text system'




```python
test1 == test2
```




    True




```python

```

3. Create a CSV file called books.csv by using these lines:

title,author,year

The Weirdstone of Brisingamen,Alan Garner,1960

Perdido Street Station,China Miéville,2000

Thud!,Terry Pratchett,2005

The Spellman Files,Lisa Lutz,2007

Small Gods,Terry Pratchett,1992



```python
import csv
rows =[ ['title','author','year'],
    ['The Weirdstone of Brisingamen','Alan Garner',1960],
    ['Perdido Street Station','China Miéville',2000],
    ['Thud!','Terry Pratchett',2005],
    ['The Spellman Files','Lisa Lutz',2007],
    ['Small Gods','Terry Pratchett',1992]]
with open('books.csv','w',newline='') as file:
    writer = csv.writer(file)
    writer.writerows(rows)
```


```python

```

4. Use the sqlite3 module to create a SQLite database called books.db, and a table called books with these fields: title (text), author (text), and year (integer).



```python
import sqlite3
```


```python
db = sqlite3.connect('books.db')
```


```python
curs = db.cursor()
```


```python
curs.execute('create table books(title varchar(20),author varchar(20), year int)')
```




    <sqlite3.Cursor at 0x290b587ece0>




```python
db.commit()

```


```python

```

5. Read books.csv and insert its data into the book table.



```python
import pandas as pd

read_books = pd.read_csv('books.csv',encoding='unicode_escape')
read_books.to_sql('books', db, if_exists='append', index = False)
```


```python

```

6. Select and print the title column from the book table in alphabetical order.



```python
curs.execute('select title from books order by title asc')
print(curs.fetchall())
```

    [('Perdido Street Station',), ('Perdido Street Station',), ('Perdido Street Station',), ('Small Gods',), ('Small Gods',), ('Small Gods',), ('The Spellman Files',), ('The Spellman Files',), ('The Spellman Files',), ('The Weirdstone of Brisingamen',), ('The Weirdstone of Brisingamen',), ('The Weirdstone of Brisingamen',), ('Thud!',), ('Thud!',), ('Thud!',)]
    


```python

```

7. From the book table, select and print all columns in the order of publication.



```python
curs.execute('select title, author,year from books order by year')
#print(curs.fetchall())

df = pd.DataFrame(curs.fetchall(), columns=['title','author','year'])
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>author</th>
      <th>year</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>The Weirdstone of Brisingamen</td>
      <td>Alan Garner</td>
      <td>1960</td>
    </tr>
    <tr>
      <th>1</th>
      <td>The Weirdstone of Brisingamen</td>
      <td>Alan Garner</td>
      <td>1960</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Small Gods</td>
      <td>Terry Pratchett</td>
      <td>1992</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Small Gods</td>
      <td>Terry Pratchett</td>
      <td>1992</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Perdido Street Station</td>
      <td>China Miéville</td>
      <td>2000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Perdido Street Station</td>
      <td>China Miéville</td>
      <td>2000</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Thud!</td>
      <td>Terry Pratchett</td>
      <td>2005</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Thud!</td>
      <td>Terry Pratchett</td>
      <td>2005</td>
    </tr>
    <tr>
      <th>8</th>
      <td>The Spellman Files</td>
      <td>Lisa Lutz</td>
      <td>2007</td>
    </tr>
    <tr>
      <th>9</th>
      <td>The Spellman Files</td>
      <td>Lisa Lutz</td>
      <td>2007</td>
    </tr>
  </tbody>
</table>
</div>




```python

```

8. Use the sqlalchemy module to connect to the sqlite3 database books.db that you just made in exercise 6.



```python
import sqlalchemy
engine = sqlalchemy.create_engine("sqlite:///books.db")
rows = engine.execute('select * from books')
for i in rows:
    print(i)
```

    ('The Weirdstone of Brisingamen', 'Alan Garner', 1960)
    ('Perdido Street Station', 'China Miéville', 2000)
    ('Thud!', 'Terry Pratchett', 2005)
    ('The Spellman Files', 'Lisa Lutz', 2007)
    ('Small Gods', 'Terry Pratchett', 1992)
    ('The Weirdstone of Brisingamen', 'Alan Garner', 1960)
    ('Perdido Street Station', 'China Miéville', 2000)
    ('Thud!', 'Terry Pratchett', 2005)
    ('The Spellman Files', 'Lisa Lutz', 2007)
    ('Small Gods', 'Terry Pratchett', 1992)
    ('The Weirdstone of Brisingamen', 'Alan Garner', 1960)
    ('Perdido Street Station', 'China Miéville', 2000)
    ('Thud!', 'Terry Pratchett', 2005)
    ('The Spellman Files', 'Lisa Lutz', 2007)
    ('Small Gods', 'Terry Pratchett', 1992)
    


```python

```

9. Install the Redis server and the Python redis library (pip install redis) on your computer. Create a Redis hash called test with the fields count (1) and name ('Fester Bestertester'). Print all the fields for test.


!pip install redis

import redis conn = redis.Redis() conn.delete('test') 1 conn.hmset('test', {'count': 1, 'name': 'Fester Bestertester'}) True conn.hgetall('test') {b'name': b'Fester Bestertester', b'count': b'1'}




```python

```

10. Increment the count field of test and print it.


conn.hincrby('test', 'count', 3) 4 conn.hget('test', 'count') b'4'


```python

```
