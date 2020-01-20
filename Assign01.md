# Unix command line

Unix command line utilities have been around for nearly half a century and they will continue to be the principal way for communicating with servers and remote systems for decades to come. All major operating systems (including Windows PowerShell) support Unix-style command line utilities.

Let's review basic usage of command line utilities for working in a Unix terminal. More specifically, we will work Linux, one the most popular derivatives of Unix. 

The are many resources to help learning Linux command-line utilities. Please go through an online tutorial if you need a refresher. This one seems decent: https://ryanstutorials.net/linuxtutorial/commandline.php 

Open the terminal window on your personal computer and use the `ssh` utility with the certificate file provided to you to log into your account on `main.data-science-ust.net`.

If your name is Bob, the connection command will be

```shell
ssh -i bob-big-data.pem bob@main.data-science-ust.net
```

Please let me know if you cannot locate your `.pem` file and I will issue you a new one. Keep the file safe and do not share it.

In class, we reviewed the basic utilities for viewing directory contents, viewing text files, navigting the folder hierarchy, creating and removing folders, creating and editing text files, deleting files, and changing access permissions. We used the `man` pages to learn about the options that each command provides. We also learned how to create and execute simple shell scripts and python programs.

Know how to use the shell commands: `pwd`, `ls`, `cd`, `cat`, `less`, `mkdir`, `rm`, `rmdir`, `chmod`, `touch`, `vi` or `nano`, `echo`, `which`, and `man`.

Understand how command options are used, e.g.
```shell
ls -la 
```

Understand how wildcards `*` work and redirection of standard output, e.g.
```shell
cat assign*txt > report.txt 
```

Learn to execute an executable program such as one of your own scripts or a pre-installed program such as `python3`.

Choose a text editor: `nano` or `vi` and learn to edit files and save them.

Understand privileges: "user", "group", and "other" for read/write/execute. 

# Assignment
Due Jan 27, 2020

To complete this assignment, perform the following 

1. Log into `main.data-science-ust.net`. Upon login, you are in your home directory, which is `/home/bob` if you are Bob. You can always go back to your home folder using `cd ~`. In paths, `~` is shorthand for your home folder. 
2. In your home directory, create a folder named `homework`. Remove the `x` permission on the folder from others so that no one else can access your work.
3. Inside `homework`, create another folder named `a01`
4. Inside `~/homework/a01`, create a text file named `data-science.txt` Edit the file and write your explanation of the principal differences between the use of the terms "statistics" and "data-science". 
5. Inside `~/homework/a01`, create a text file named `big-data.txt`. Edit the file and write your explanation of the defining characteristics of Big Data technologies. 
6. Create a file named `combine` that will become an executable bash script, containing one or more command lines. The script will combine the two text files into one.  The contents of the files should be
```shell
#!/bin/bash
echo "# Chapter 1" > out.md
cat data-science.txt >> out.md
echo -e "\n# Chapter 2" >> out.md
cat big-data.txt >> out.md
```
7. Change the permissions on `combine` to make it executable.
8. Execute `commbine` by entering  the command
```
./combine
```
This will produce the file `out.md`.
9. Use the `less` command to review the contents of `out.md`. Exit by pressing "q".
10. Create a file named `count.py` and write a python program that reads `out.md` and prints the number of sentences. Add the the path to the python interpreter in its first line as in
```python
#!/usr/bin/python3
print("Hello world!")
```
Make `count.py` executable by changing its permissions and run it as 
```shell
./count.py
```
11. Finally add `./count.py >> out.md` as the last line of `./combine` and re-run `./combine`. You can verify that it work by reviewing `out.md`

The  assignment by verifying the contents of `out.md` and `count.py`
