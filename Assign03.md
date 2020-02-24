# Assignment 3: Regular Expressions, Git, and a Business Case

## Regular expressions
Learn to use *regular expressions*. Resources:
* https://regexone.com/lesson/introduction_abcs
* https://www.kaggle.com/sohier/introduction-to-regular-expressions
* https://www.guru99.com/python-regular-expressions-complete-tutorial.html

## Git 
Learn the principles of `git` and its usage from the command line. 
* Git Handbook https://guides.github.com/introduction/git-handbook/
* Learning Git: https://learngitbranching.js.org/

## Example of Big Data: SiteZeus 
* [Video 1](https://www.youtube.com/watch?v=c4m4HH19m5Q) -- Model basics and adding data 
* [Video 2](https://www.youtube.com/watch?v=CuihDgBtApI) -- Predictive model 
* [Video 3](https://www.youtube.com/watch?v=OHGxfjNzIHY) -- SiteZeus + Uber Media on cell phone data

# Assignment
Accepting the homework link sent to you in class, you will fork the private repo https://github.com/MSDS-6311/MSDS-6311-A03. This creates a new repo, for example https://github.com/MSDS-6311/msds6311a3-meganwright612 for Megan. In class, you learned how to clone the repo from the command line to a host machine, e.g. the cloud instance or your personal computer.

In this assignment, you will learn parts of the workflow working with `git` repositories.

### 1. Pull updates from the "upstream" repo 

Read about the concept of remote repos in `git`.

In your cloned directory, use the `git remote` commands to view currently configured remotes. 
```shell
git remote -v
```
Initially, you will only have one remote called `origin`.

Let's add a new remote called `upstream` pointing to the original source of the assignment from which your repo was forked.
```shell
git remote add upstream https://github.com/MSDS-6311/MSDS-6311-A03
```
This will enable you to pull changes made to that repository since you initially cloned it:
```shell
git pull upstream master 
```
At this point, `git` will merge the upstream changes. If there are conflicts, it will indicate which files must e edited to resolve the conflict.

To see the current status of your repository, use 
```
git status
```

To commit your changes, use
```
git add -u
git commit
```
This will  bring up an editor to edit the commit message.

After a successful commit, you can push the changes back to your repository with the command

```
git push
```

Then you can review the contents of your repository on `GitHub.com`.


Follow the instructons in the `README` file (front page of the repo) to complete the assignment.



