1. How do you distinguish between shutil.copy() and shutil.copytree()?


shutil.copy : Copies a single file
    
shutil.copytree() : will copy an entire folder and every folder and file contained in it


```python

```

2. What function is used to rename files?



```python
import os
os.rename("text.txt","testnew.txt")
```


```python

```

3. What is the difference between the delete functions in the send2trash and shutil modules?


The shutil module’s rmtree() function can be used to delete files or folders. But, this function delete the files
permanently.The operations cannot be undone if there were any accidental deletions performed 

Using send2trash, we can send files to the Trash or Recycle Bin instead of permanently 
deleting them.
If the directory contains files or other folders, those are also deleted. A TrashPermissionError exception is raised, 
in case a file could not be deleted due to permission error or any other unexpected reason.



```python

```

4. ZipFile objects have a close() method just like File objects’ close() method. What ZipFile method is equivalent to File objects’ open() method?


The zipfile.ZipFile() function is equivalent to the open() function; the first argument is the filename, and the second argument is the mode to open the ZIP file in (read, write, or append).


```python
from zipfile import Zipfile
with ZipFile(file_name, 'r') as zip
```


```python

```

5. Create a programme that searches a folder tree for files with a certain file extension (such as .pdf or .jpg). Copy these files from whatever location they are in to a new folder.


```python
# Write a program that walks through a folder tree 
# and searches for files with a certain file extension (such as .pdf or .jpg).
# Copy these files from whatever location they are in to a new folder.
import os, shutil

def selectiveCopy(source, extensions, destFolder):
    folder = os.path.abspath(source)
    destFolder = os.path.abspath(destFolder)
    print('Looking in', source, 'for files with extensions of', ', '.join(extensions))
    for foldername, subfolders, filenames in os.walk(source):
        for filename in filenames:
            name, extension = os.path.splitext(filename)
            if extension in extensions:
                fileAbsPath = foldername + os.path.sep + filename
                print('Coping', fileAbsPath, 'to', destFolder)
                shutil.copy(fileAbsPath, destFolder)

extensions = ['.pdf','.jpg']
source = "C:\\Users\\dhira\\Desktop\\source"
destFolder = "C:\\Users\\dhira\\Desktop\\destination"
selectiveCopy(source, extensions, destFolder)
```

    Looking in C:\Users\dhira\Desktop\source for files with extensions of .pdf, .jpg
    Coping C:\Users\dhira\Desktop\source\Dhiral_CV.pdf to C:\Users\dhira\Desktop\destination
    Coping C:\Users\dhira\Desktop\source\IMG_20160326_114723150.jpg to C:\Users\dhira\Desktop\destination
    


```python

```
