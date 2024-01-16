# Lab Report 1
## ls Command
**With no argument:**
```
[user@sahara ~/lecture1]$ ls
Hello.class  Hello.java  messages  README
[user@sahara ~/lecture1]$ pwd
/home/lecture1
```
Working directory when command was ran: /home/lecture1

The reason why I got the output of the terminal printing "Hello.class Hello.java messages README" was because the ls command also known as the list command, prints the list of files and folders in the given path but in this case since there was no argument, the ls command printed the list from the current directory. 

This output was not an error because the command did what it was supposed to do.

**With a path to a directory as an argument:**
```
[user@sahara ~/lecture1]$ ls messages/
en-us.txt  es-mx.txt  ru.txt  zh-cn.txt
[user@sahara ~/lecture1]$ pwd
/home/lecture1
```
Working directory when command was ran: /home/lecture1

The reason why I got the output of the terminal printing a list of text files was because since the ls command prints a list of files and folders from a given path which in this case was the messages directory, the terminal printed the list of the text files from messages.

This was not an error because the command worked like it was supposed to which was to print the list. 
**With a path to a file as an argument:**
```
[user@sahara ~/lecture1/messages]$ ls en-us.txt 
en-us.txt
```
## cd Command
**With no argument:**
```
[user@sahara ~/lecture1]$ cd
```
**With a path to a directory as an argument:**
```
[user@sahara ~/lecture1]$ cd messages/
[user@sahara ~/lecture1/messages]$
```
**With a path to a file as an argument:**
```
[user@sahara ~/lecture1]$ cd Hello.java 
bash: cd: Hello.java: Not a directory
```

