-------------------------------------------------------------------------------

# How to create a text file

## Step-1 :
```
f= open("banuprakash.txt","w+")
```

* We declared the variable f to open a file named ***"banuprakash.txt"***. Open takes 2 arguments, the file that we want to open and a string that represents the kinds of permission or operation we want to do on the file

* Here, we used "w" letter in our argument, which indicates write and will create a file if it does not exist in library
Plus sign indicates both read and write.

* The available option beside "w" are, "r" for read, and "a" for append

## Step-2 :
```
for i in range(10):
  f.write("This is line %d\r\n" % (i+1))
```
     
* We have a for loop that runs over a range of 10 numbers.

* Using the write function to enter data into the file.

* The output we want to iterate in the file is "this is line number", which we declare with write function and then percent d (displays integer)

* So basically we are putting in the line number that we are writing, then putting it in a carriage return and a new line character

## Step-3 :

```
f.close()
```

This will close the instance of the file ***banuprakash.txt*** stored

Once the below code is executed, ***banuprakash.txt*** file has been created:

!["file1"](https://raw.githubusercontent.com/banuprakashm/python-tutorials-problems/master/images/file/file1.png)

When you click on your text file in our case ***"banuprakash.txt"*** it will look something like this

![](https://raw.githubusercontent.com/banuprakashm/python-tutorials-problems/master/images/file/file2.png)

-------------------------------------------------------------------------------
# How to Append data to a file :

You can also append a new text to the already existing file or the new file. Append simply adds the new text to the next line it does not overwrite a file.

## Step-1 :
```
f=open("banuprakash.txt", "a+")
```
Once again if you could see a plus sign in the code, it indicates that it will create a new file if it does not exist. But in our case we already have the file, so we are not required to create a new file.

## Step-2 :
```
for i in range(2):
	f.write("Appended line %d\r\n" % (i+1))
```

This will write data into the file in append mode,  :

![](https://raw.githubusercontent.com/banuprakashm/python-tutorials-problems/master/images/file/file3.png)

You can see the output in ***"banuprakash.txt"*** file. The output of the code is that earlier file is appended with new data.

![](https://raw.githubusercontent.com/banuprakashm/python-tutorials-problems/master/images/file/file4.png)

-------------------------------------------------------------------------------
# How to read a file :

## Step-1 : Open the file in Read mode
```
f=open("banuprakash.txt", "r")

```

## Step-2 : We use the mode function in the code to check that the file is in open mode. If yes, we proceed ahead
```
if f.mode == 'r':
```
## Step-3 : Use f.read to read file data and store it in variable content
```
contents =f.read()
```
	
## Step-4 : print contents 
```
print(contents)
```
Code for read a file :

![](https://raw.githubusercontent.com/banuprakashm/python-tutorials-problems/master/images/file/file5.png)

Output:

![](https://raw.githubusercontent.com/banuprakashm/python-tutorials-problems/master/images/file/file6.png) 

-------------------------------------------------------------------------------

Mode          | Description
------------- | -------------
'r'           | This is the default mode. It Opens file for reading.
'w'           | This Mode Opens file for writing. If file does not exist, it creates a new file.If file exists it truncates the file.
'x'           | Creates a new file. If file already exists, the operation fails.
'a'           | Open file in append mode. If file does not exist, it creates a new file.
't'           | This is the default mode. It opens in text mode.
'+'           | This will open a file for reading and writing (updating)

-------------------------------------------------------------------------------

Methods .         | Description
------------- | -------------
close()       | Close an open file. It has no effect if the file is already closed.
detach()      | Separate the underlying binary buffer from the ```TextIOBase``` and return it.
fileno()      | Return an integer number (file descriptor) of the file.
flush()       | Flush the write buffer of the file stream.
isatty()      | Return ```True``` if the file stream is interactive.
read(```n```) | Read atmost ```n``` characters form the file. Reads till end of file if it is negative or ```None```.
readable()            | Returns ```True``` if the file stream can be read from.
readline(```n```= -1) | Read and return one line from the file. Reads in at most ```n``` bytes if specified.
readlines(```n```= -1) | Read and return a list of lines from the file. Reads in at most ```n``` bytes/characters if specified.
seek(```offset```,```from=SEEK_SET```)       | Change the file position to ```offset``` bytes, in reference to ```from``` (start, current, end).
seekable()       | Returns ```True``` if the file stream supports random access.
tell()       | Returns the current file location.
truncate(size=None)       | Resize the file stream to ```size``` bytes. If ```size``` is not specified, resize to current location.
writable()       | Returns ```True``` if the file stream can be written to.
write(```s```)       | Write string ```s``` to the file and return the number of characters written.
writelines(```lines''')       | 	Write a list of ```lines``` to the file.


-------------------------------------------------------------------------------
