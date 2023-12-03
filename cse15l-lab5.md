# Lab Report 5
### Original post

#### John Smith | Dec 1, 2023 9:41am
##### Hey Everyone,
##### I'm stuck trying to figure out this bug that is displayed in the screenshot below. I can't seem to figure out how to resolve it. I've been working on a Java program that reads a text file and prints each line with line numbers. I wrote a Bash script to compile and run the program, but the output isn't what I expected. Instead of numbering the lines, it just prints the contents of the file without any numbers.
##### Below is a screenshot of the output I'm getting:
##### [Insert screenshot]
##### I think the issue might be with the way I'm reading the file in Java, or maybe how I'm passing the filename to the Java program in the Bash script. I'm using the command `bash run.sh test.txt` to run the script.
##### Any help would be greatly appreciated!

___

### Response from TA

#### John Appleseed | Dec 1, 2023 2:41pm
##### Hey John,
##### It seems like the issue could be within the Java code or the bash script. Can you try running the Java code with the command 'java LineNumber test.txt' and see if it works as intended? Hopefully by doing this, we can isolate where your issue is coming from and proceed from there.
##### Good luck!

___
### Response from student

#### John Smith | Dec 1, 2023 9:41pm
##### I ran the program with the command you provided and everything worked as intended! I put a screenshot below:
##### [Insert screenshot]
##### So after isolating the issue, it does seem to be coming from the bash script itself. I've been trying to figure it out, but just in case you have any suggestions, I put the bash script below:
##### [Insert screenshot of bash script]
