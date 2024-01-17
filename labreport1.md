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

I think that it is a small error because the terminal returns a message that says the Hello.java file is not a directory therefore you cannot switch to that directory because it is a file. 

## cat Command
**With no argument:**
```
[user@sahara ~/lecture1]$ cat


[user@sahara ~/lecture1]$ pwd
/home/lecture1

```
Working directory when command was ran: standard input output

The reason why I had the output of the user in the terminal disappearing after using the cat command without an agumentis because when you use the cat command without an argument, it makes the terminal read from standard input output which is why there is no user@sahara. You then can use ctrl + D to exit out of the standard input output mode and return to the normal terminal mode. 

This output was not an error because there was nothing wrong with the terminal when I ran the cat command and because I was able to get the terminal back to norrmal. 

**With a path to a directory as an argument:**
```
[user@sahara ~/lecture1]$ cat messages/
cat: messages/: Is a directory
[user@sahara ~/lecture1]$ pwd
/home/lecture1
```
Working directory when command was ran: /home/lecture1

The reason why I had the output of the terminal returning a message saying "cat: messages/: Is a directory" is because the cat command aka concatenate, prints whatever file you give it for the argument and since I gave it a directory hence why it says it is a directory, this is why it didnt work because it needs to be a file. 

I think this is a small error because the terminal gives a message saying that he command doesnt work because the path is a directory.

**With a path to a file as an argument:**
```
[user@sahara ~/lecture1]$ cat messages/en-us.txt 
Hello World!
[user@sahara ~/lecture1]$ pwd
/home/lecture1
```
Working directory when command was ran: /home/lecture1

The reason why I got the output of the terminal printing "Hello World!" is because since the cat command prints the contents of a file, because I used the path messages/en-us.txt, it printed whhat was in the en-us.txt file which was Hello world. 
The working directory also never changed because we are only looking at the contents and not changing anything.

This was not an error as this was supposed to happpen.

