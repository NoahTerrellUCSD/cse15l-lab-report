# Lab Report 1
## ls Command
With no argument:
```
[user@sahara ~/lecture1]$ ls
Hello.class  Hello.java  messages  README
```
With a path to a directory as an argument:
```
[user@sahara ~/lecture1]$ ls messages/
en-us.txt  es-mx.txt  ru.txt  zh-cn.txt
```
With a path to a file as an argument:
```
[user@sahara ~/lecture1/messages]$ ls en-us.txt 
en-us.txt
```
## cd Command
With no argument:
```
[user@sahara ~/lecture1]$ cd
```
With a path to a directory as an argument:
```
[user@sahara ~/lecture1]$ cd messages/
[user@sahara ~/lecture1/messages]$
```
With a path to a file as an argument:
```
[user@sahara ~/lecture1]$ cd Hello.java 
bash: cd: Hello.java: Not a directory
```

