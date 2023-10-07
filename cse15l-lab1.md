# Lab Report 1

<br>
## Share an example of using the commands with no arguments

### An example of cd command with no argument
  ```bash
  [user@sahara ~]$ cd
  [user@sahara ~]$
  ```

### An example of ls command with no argument
  ```bash
  [user@sahara ~]$ ls
  lecture1
  [user@sahara ~]$ 
  ```

### An example of cat command with no argument</summary>
  ```bash
  [user@sahara ~]$ cat
  ^C
  [user@sahara ~]$ 
  ```

<br>
## Share an exmaple of using the command with a path to a directory as an argument.

### An example of cd command with a path to a directory as an argument
  ```bash
  [user@sahara ~]$ cd lecture1/messages
  [user@sahara ~/lecture1/messages]$ 
  ```

### An example of ls command with a path to a directory as an argument
  ```bash
  [user@sahara ~]$ ls lecture1/messages
  en-us.txt  es-mx.txt  pt-br.txt  zh-cn.txt      
  [user@sahara ~]$ 
  ```

### An example of cat command with a path to a directory as an argument
  ```bash
  [user@sahara ~]$ cat lecture1/messages
  cat: lecture1/messages: Is a directory
  [user@sahara ~]$ 
  ```

<br>
## Share an example of using the command with a path to a file as an argument.

### An example of cd command with a path to a file as an argument
  ```bash
  [user@sahara ~]$ cd lecture1/messages/en-us.txt
  bash: cd: lecture1/messages/en-us.txt: Not a directory
  [user@sahara ~]$ 
  ```
  
### An example of ls command with a path to a file as an argument
  ```bash
  [user@sahara ~]$ ls lecture1/messages/en-us.txt
  lecture1/messages/en-us.txt
  [user@sahara ~]$ 
  ```
### An example of cat command with a path to a file as an argument
  ```bash
  [user@sahara ~]$ cat lecture1/messages/en-us.txt
  Hello World!
  [user@sahara ~]$ 
  ```
