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
[user@sahara ~/lecture1/messages]$ pwd
/home/lecture1/messages
```
Working directory when command was ran: /home/lecture1/messages

The reason why I got the output of the terminal printing "en-us.txt" was because when you use the ls command for a file, all it does it print the file name. 

This output was not an error because it did what it was supposed to which was return the file name. 

## cd Command
**With no argument:**
```
[user@sahara ~/lecture1]$ cd
[user@sahara ~]$ pwd
/home
```
Working directory when command was ran: /home

The reason why I got the output of nothing and the working directory to change from /home/lecture1 to /home was because when you use the cd command by itself, it returns you to the home directory. 

This was not an error because this was the correct output. 

**With a path to a directory as an argument:**
```
[user@sahara ~/lecture1]$ cd messages/
[user@sahara ~/lecture1/messages]$ pwd
/home/lecture1/messages
```
Working directory when command was ran: /home/lecture1/messages

The reason why I got the output of the current directory changing to the messages directory is because the cd command is the change directory command which is used to switch the current working directory to a given path which in this case is the messages directory. 

This was not an error because this is suppoesed to happen. 

**With a path to a file as an argument:**
```
[user@sahara ~/lecture1]$ cd Hello.java 
bash: cd: Hello.java: Not a directory
[user@sahara ~/lecture1]$ pwd
/home/lecture1
```
Working directory when command was ran: /home/lecture1

The reason why I got the output of a terminal message saying "bash: cd: Hello.java: Not a directory" was because the cd command doesnt work on a file since the command can only switch to a file directory hence why the message said it was not a directry.

I dont think that this was an error because nothing bad happened to the program it only told me that the specific command with a file path doesnt work. 

## cat Command
**With no argument:**
```

```
Working directory when command was ran: 

**With a path to a directory as an argument:**
```

```
