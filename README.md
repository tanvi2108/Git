Git Exercise
The following practical exercises should give you some familiarity with using Git.

Note: The provided command line examples are to remind you of the correct syntax and keywords, and won't necessarily work if you type them in blindly

Other Note: to get help on a particular git command, use git <command> --help

Setup
Install and setup git on your computer (remember to set your name/email)

$ git config --global user.name "Firstname Lastname"
$ git config --global user.email "example@maths.ox.ac.uk"
Create an account (or login) to GitHub at https://github.com

(optional) Generate a ssh-key and add it to your GitHub account (for more information see https://help.github.com/articles/connecting-to-github-with-ssh/)

$ ssh-keygen -t rsa -C "email@address.com"
$ cat ~/.ssh/id_rsa.pub
Fork this repository: https://github.com/deespacelab/Git

Exercise 1: Making Commits
Clone the forked repository to your computer

$ git clone <url>
Create and add a new file

$ git add <file>
Commit the new file

$ git commit -m "message"
Examine the state of your repo with git status.

$ git status
Edit and save your new file, then add it to the staging area. Finally make a new commit with the edited file. At all stages use git status to see how your repository changes

$ git add <file>
$ git commit -m "message"
Make some more commits and view the log

$ git log 
Commit everything you have done so far

$ git commit -a -m "message"
Push the commits to the server

$ git push
Exercise 2: Branching and Merging
Create a new branch

$ git checkout -b new_branch
Edit your new file and commit the result

Swap back to the master branch

$ git checkout master
Merge new_branch to master

$ git merge new_branch
Now create conflicting commits in new_branch and master and try to merge them. Note the conflict-resolution markers will look something like this.

<<<<<<< HEAD
This is the new line in master
=======
This is the new line in branch
>>>>>>> branch
resolve the conflict (i.e. edit the conflict markers to match how you want the file to look like) and commit the result. Use git log to see the resulting commits on the master branch.

Exercise 3: Collaboration
Push the new branch that you created in the previous exercise to your remote repository

$ git push origin new_branch
Get the person sitting next to you to clone your repository and checkout your new branch.

$ git checkout --track origin/new_branch
Both of you make commits to the new branch. Have one person push their commits to the remote and the other merge these with their own commits. Swap roles and repeat the process.

Once you are happy with the state of your new branch, merge it onto your master branch and bask in the glow of your new Git skills.
