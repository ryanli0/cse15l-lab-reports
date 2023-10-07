![Image](Purisma-2.png)

<br>

## Share an example of using the commands with no arguments

### An example of cd command with no argument
  ```bash
  [user@sahara ~]$ cd
  [user@sahara ~]$
  ```
##### Working Directory: /home
##### What command meant: Change directory but no directory was given
##### Error?: No, this can also be used to bring the terminal back to root directory

### An example of ls command with no argument
  ```bash
  [user@sahara ~]$ ls
  lecture1
  [user@sahara ~]$ 
  ```
##### Working Directory: /home
##### What command meant: List files in working directory
##### Error?: No

### An example of cat command with no argument</summary>
  ```bash
  [user@sahara ~]$ cat
  ^C
  [user@sahara ~]$ 
  ```
##### Working Directory: /home
##### What command meant: Concatenate working directory but since no file could be read, command needed a manual break
##### Error?: No, but it would have caused the command to run forever, not allowing another command without a manual break

<br>
<br>

## Share an exmaple of using the command with a path to a directory as an argument.

### An example of cd command with a path to a directory as an argument
  ```bash
  [user@sahara ~]$ cd lecture1/messages
  [user@sahara ~/lecture1/messages]$ 
  ```
##### Working Directory: /home/lecture1/messages
##### What command meant: Change directory to messages directory
##### Error?: No, it worked as expected and changed directory

### An example of ls command with a path to a directory as an argument
  ```bash
  [user@sahara ~]$ ls lecture1/messages
  en-us.txt  es-mx.txt  pt-br.txt  zh-cn.txt      
  [user@sahara ~]$ 
  ```
##### Working Directory: /home
##### What command meant: List files within messages directory
##### Error?: No, it properly listed files within the directory specified

### An example of cat command with a path to a directory as an argument
  ```bash
  [user@sahara ~]$ cat lecture1/messages
  cat: lecture1/messages: Is a directory
  [user@sahara ~]$ 
  ```
##### Working Directory: /home
##### What command meant: Concatenate messages directory but since it's a directory and not a file, it returned an error
##### Error?: Yes, it gave an error due to an improper usage of the cat command on a directory instead of a file

<br>
<br>

## Share an example of using the command with a path to a file as an argument.

### An example of cd command with a path to a file as an argument
  ```bash
  [user@sahara ~]$ cd lecture1/messages/en-us.txt
  bash: cd: lecture1/messages/en-us.txt: Not a directory
  [user@sahara ~]$ 
  ```
##### Working Directory: /home
##### What command meant: Change directory to en-us.txt but since en-us.txt is a file and not a directory, it returned an error
##### Error?: Yes, it gave an error due to an improper usage of the cd command on a file instead of a directory
  
### An example of ls command with a path to a file as an argument
  ```bash
  [user@sahara ~]$ ls lecture1/messages/en-us.txt
  lecture1/messages/en-us.txt
  [user@sahara ~]$ 
  ```
##### Working Directory: /home
##### What command meant: list files within en-us.txt but since there was nothing else to list, it printed file path
##### Error?: While not really doing anything, it didn't result in an error since it had something to print which was the file path of the specified file

### An example of cat command with a path to a file as an argument
  ```bash
  [user@sahara ~]$ cat lecture1/messages/en-us.txt
  Hello World!
  [user@sahara ~]$ 
  ```
##### Working Directory: /home
##### What command meant: Concatenate contents of en-us.txt which returned the contents of the txt file (Hello World!)
##### Error?: No
