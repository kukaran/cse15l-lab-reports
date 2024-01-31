Lab Report 1
Kumail Karan
A17688437

For terminal command `cd`:

When inputted with no arguments:

```
[user@sahara ~]$ cd
[user@sahara ~]$
```

Working Directory (Absolute path): The working directory is the `/home` directory. (Only one directory posseses this name)

Explanation: When inputted with no arguments, the `cd` command does nothing, UNLESS you are not in the `/home` directory. If your working directory is not the `/home` directory then using the `cd` command will change your working directory to the `/home` directory. 

Error?: Not an Error.


When inputted with a path to a directory as an argument:

```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$
```

Working Directory (Absolute Path): Moved from `/home` to `/home/lecture1` directory as a result of using the `cd` command.

Explanation: When inputted with a directory as an argument, in this case `lecture1` was the argument, then you move to operating within that directory. It also indicates that with `/lecture1` being displayed after the `~`.

Error?: Not an Error.


When inputted with a path to a file as an argument:

```
[user@sahara ~]$ cd lecture1/Hello.java
bash: cd: lecture1/Hello.java: Not a directory
```

Working Directory (Absolute Path):  `/home`

Explanation: When inputted with a file as an argument, in this case the file is `Hello.java`, then an error appears, stating that the inputted path does not lead to a directory. This happens because the `cd` command is meant to change to other directories or folders, not directly lead to files. 

Error?: Yes this is an error, you cannot use the `cd` command and have the argument be a file, files are not directories and therefore do not contain or have the capacity to contain other files.





For terminal command `ls`:

When inputted with no arguments:

```
[user@sahara ~]$ ls 
lecture1
```

Working Directory (Absolute Path): `/home`

Explanation: When inputted with no arguments, the `ls` command lists all the files and directories within the current directory that you are in, in this case it shows that the `home`
directory has one directory called `lecture1` contained in it.

Error?: Not an Error.


When inputted with a path to a directory as an argument:

```
[user@sahara ~]$ ls lecture1
Hello.class  Hello.java  messages  README
```

Working Directory (Absolute Path): `/home`

Explanation: When inputted with a path to a directory as an argument, the `ls` command lists out all the directories and files within that argument, in this case it showed all the files contained within `lecture1`.

Error?: Not an error.


When inputted with a path to a file as an argument:

```
[user@sahara ~]$ ls lecture1/Hello.java
lecture1/Hello.java
```

Working Directory (Absolute Path): `/home`

Explanation: When inputted with a path to a file as an argument, in this case `lecture1/Hello.java`, all the `ls` command does is print out the path to the file that I originally inputted as an argument. 

Error?: Not an error.





For terminal command `cat`:

When inputted with no arguments:

```
[user@sahara ~]$ cat
Print
Print
```

Working Directory (Absolute Path): `/home`

Explanation: When the `cat` command is inputted with no argument, the terminal gets rid of the part of the command line indicating the device and directory, `[user@sahara ~]$`, is now gone. Afterwards I'm left with a blank slate and am allowed to type anything I want, with the result being printed again when I hit enter. In this case I typed `Print` and when I clicked enter, `Print` was displayed again on the command line. To exit this process and get back to the original command line, I can hit the keys Control and C simultaneously on my keyboard (Macbook).

Error?: Not an error.


When inputted with a path to a directory as an argument:

```
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
```

Working Directory (Absolute Path): `/home`

Explanation: When the `cat` command is inputted with a path to a directory as an argument, an error is displayed stating that the inputted path is a directory, in this case the directory being `lecture1`. This shows up because the `cat` command is used typically to concatenate or print out the contents of a file. However, if the argument is a directory, then the `cat` command cannot print anything out.

Error?: Yes, there is an error. If the `cat` is used on a directory, then it cannot concatenante anything as the argument is not a file with content that is able to be printed out.


When inputted with a path to a file as an argument:

```
[user@sahara ~]$ cat lecture1/Hello.java
import java.io.IOException;
import java.nio.charset.StandardCharsets;
import java.nio.file.Files;
import java.nio.file.Path;
public class Hello {

  public static void main(String[] args) throws IOException {
  
    String content = Files.readString(Path.of(args[0]), StandardCharsets.UTF_8);
    
    System.out.println(content);
    
 }
 ```

Working Directory (Absolute Path): `/home`

Explanation: When the `cat` command is inputted with a path to a file as an argument, the `cat` command prints out the contents of the file. In this case the contents of `Hello.java` is printed out.

Error?: Not an error.




