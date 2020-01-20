# Assignmnet 1 

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

Know how to use the shell commands: `pwd`, `ls`, `cd`, `cat`, `less`, `mkdir`, `rm`, `rmdir`, `chmod`, `touch`, `vi` or `nano`, `echo`, and `man`.

Understand how command options are used, e.g.
```shell
ls -la 
```

Understand how wildcards `*` work and redirection of standard output, e.g.
```shell
cat assign*txt > report.txt 
```

Choose a text editor: `nano` or `vi` and learn to edit files and save them.

To complete the assignment, 
