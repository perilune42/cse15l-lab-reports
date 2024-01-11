This web page describes the behavior of the `cd`, `ls`, and `cat` commands.

---
# `cd`: Change Directory
No arguments:
```
[user@sahara ~/lecture1]$ cd
[user@sahara ~]$
```
*Working directory:* `/home/lecture1` \
Changes the working directory to `/home` by default when no argument are provided. \
**No Errors**
***
Directory as argument: 
```
[user@sahara ~/lecture1]$ cd messages/
[user@sahara ~/lecture1/messages]$
```
*Working directory:* `/home/lecture1` \
Changes the working directory to the provided argument `messages/`. \
**No Errors**
***
File as argument:
```
[user@sahara ~/lecture1]$ cd Hello.java
bash: cd: Hello.java: Not a directory
[user@sahara ~/lecture1]$ 
```
*Working directory:* `/home/lecture1` \
**Error:** Returns an error stating `Hello.java` is not a directory. This is because `cd` only works when changing to a directory.
***
# `ls`: List Current Directory
No arguments:
```
[user@sahara ~/lecture1]$ ls
Hello.class  Hello.java  messages  README
[user@sahara ~/lecture1]$ 
```
*Working directory:* `/home/lecture1` \
Lists out the files and folders in the working directory. \
**No Errors**
***
Directory as argument: 
```
[user@sahara ~/lecture1]$ ls messages/
en-us.txt  eo.txt  es-mx.txt  zh-cn.txt
[user@sahara ~/lecture1]$ 
```
*Working directory:* `/home/lecture1` \
Lists out the files and folders in the provided directory `messages/`. \
**No Errors**
***
File as argument:
```
[user@sahara ~/lecture1]$ ls Hello.java
Hello.java
[user@sahara ~/lecture1]$ 
```
*Working directory:* `/home/lecture1` \
Returns the name of the provided file only, as the argument is not a directory. \
**No Errors**
***
# `cat`: Concatenate
No arguments:
```
[user@sahara ~/lecture1]$ cat

```
*Working directory:* `/home/lecture1` \
Awaits any input from the user, then returns any input text back to the terminal. \
**No Errors**
***
Directory as argument: 
```
[user@sahara ~/lecture1]$ cat messages/
cat: messages/: Is a directory
[user@sahara ~/lecture1]$ 
```
*Working directory:* `/home/lecture1` \
**Error:** Returns an error stating the input `messages\` is a directory. This is because cat can only be used with files or without arguments.
***
File as argument:
```
[user@sahara ~/lecture1]$ cat messages/en-us.txt 
Hello World!
[user@sahara ~/lecture1]$ 
```
*Working directory:* `/home/lecture1` \
Concatenates and outputs all text in the given file `messages/en-us.txt`. \
**No Errors**
***

