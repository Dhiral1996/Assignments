1. What advantages do Excel spreadsheets have over CSV spreadsheets?


Excel advantages over CSV
1. It is a binary file that holds information about all the worksheets in a workbook
2. An Excel not only stores data but can also do operations on the data
3. Files saved in excel cannot be opened or edited by text editors
4. large files user is much easier in Excel for the end user. Also, 
    you can have additional functions like selecting individual cells for import, 
    convert dates and time automatically, reading formulas and their results, filters, sorting, etc
5. Apart from text, data can also be stored in form of charts and graphs
6. Excel can connect to external data sources to fetch data. You can use custom add-in in Excel to increase its functionality. 
7. Excel allows for Review of Data with detailed tracking and commenting feature
8. In Excel, spreadsheets can have values of data types other than strings; cells can have different fonts, sizes, 
   or color settings; cells can have varying widths and heights; adjacent cells can be merged


```python

```

2.What do you pass to csv.reader() and csv.writer() to create reader and writer objects?


We pass a File object, obtained from a call to open().



```python
import csv
exFile = open('example.csv')
exreader = csv.reader(exFile)
exData = list(exreader)
exData
```


```python

```

3. What modes do File objects for reader and writer objects need to be opened in?


File objects need to be opened in read-binary ('rb') for Reader objects and write-binary ('wb') for Writer objects



```python

```

4. What method takes a list argument and writes it to a CSV file?


    The writerow() method



```python

```

5. What do the keyword arguments delimiter and line terminator do?


The delimiter argument changes the string used to separate cells in a row. 

The lineterminator argument changes the string used to separate rows.



```python
import csv
csvFile = open('example.csv', 'w', newline='')
csvWriter = csv.writer(csvFile, delimiter='\t', lineterminator='\n\n')
```


```python

```

6. What function takes a string of JSON data and returns a Python data structure?


json.loads()


```python

```

7. What function takes a Python data structure and returns a string of JSON data?


json.dumps()



```python

```
