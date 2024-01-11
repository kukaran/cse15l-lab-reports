Lab Report 1:

For terminal command cd:

When inputted with no arguments:
[user@sahara ~]$ cd
[user@sahara ~]$ 

Explanation: When inputted with no arguments, the cd command does nothing, this is because the cd command is used to change the directory you are working in, (cd stands for "change directory").
             However, when you have no arguments, then you have no directory to change to, therefore nothing happens.

When inputted with a path to a directory as an argument:
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$ 

Explanation: When inputted with a directory as an argument, then you move to operating within that directory. This is exactly what the cd command was intended for. 

When inputted with a path to a file as an argument:
[user@sahara ~]$ cd lecture1/Hello.java
bash: cd: lecture1/Hello.java: Not a directory

Explanation: When inputted with a file as an argument, then an error appears, stating that the inputted path does not lead to a directory. This happens because the "cd" command is meant to change to other 
             directories or folders, not directly lead to files. 

For terminal command ls:

When inputted with no arguments:
[user@sahara ~]$ ls 
lecture1

Explanation: When inputted with no arguments, the "ls" command lists all the files and directories within the current directory that you are in. 

When inputted with a path to a directory as an argument:
[user@sahara ~]$ ls lecture1
Hello.class  Hello.java  messages  README

Explanation: When inputted with a path to a directory as an arugment, the "ls" command lists out all the directories and files within that argument (directory inputted).

When inputted with a path to a file as an argument:
[user@sahara ~]$ ls lecture1/Hello.java
lecture1/Hello.java

