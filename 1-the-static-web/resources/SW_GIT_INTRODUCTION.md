# Git

A distributed version control system for keeping a history of your code.

# Github

A software as a service (SASS) that allows your to back up your repository to the cloud and share it with other software developers.

## Create a repository
+ Log in to your account on GitHub
+ In the upper right hand corner, look for this:
<img src="../images/github-add-repo.jpg" alt="github add repo" style="width: 125px;"/>
Click the `plus` sign to create a new repository (i.e. `my-blog`)
+ Click green btn
+ Highlight https button
+ Make sure the *Create a README* options is not ticked. Then have them copy pasta the standard commands that Github provides once the repo is created.
+ Follow first set of instrux to copy commands to clipboard

##### _Example: Do not use these commands_
```
echo "# My Blog" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:username/my-blog.git
git push -u origin master
```
+ In your terminal (`workspace`) paste the copied commands and hit enter
+ type `ls -a` to see all the files, even hidden ones in your folder. You can see the `.git` folder that contains all the git magic for your `/my-blog` repo

## Set up your credentials (First time users)
+ After pasting in the commands from GitHub, you will be presented with a prompt to add the email associated with your GitHub account and your name (not your username, just i.e. "Jane Doe")
+ Copy these one by one, paste into the command line and change the placeholder info to your info
+ Type `git config --global -l`  to see if your config settings saved properly

To store credentials locally, use this command so that you're not prompted every time you push:

`git config credential.helper store`

If you don't want to store them per project, but rather globally in your HOME directory, use this instead.

`git config --global credential.helper store`

## Add, commit, push
+ Type `git status` to see the files you hav added/deleted/modified
+ `git add` plus name of file you want to add to the staging area
+ `git commit -m "my commit message"` to commit the staged areas to git
+ `git push -u origin master` to push the latest commit(s) to your repo on GitHub. After this longhand command, you can use just `git push`  
+ `git log` to see all of your commits for this repo. `q` to quit git log (if log is long enough)

## Handling merge conflicts

When a developer wants to merge a branch into master, and there has been code added or changed on a line where code currently exists, that creates a merge conflict.

##### Original code in master

```js
1. for (var i = 0; i < myArray.length; i++) {
2.   if (myArray[i].length === 3) {
3.     console.log("This is a short word");
4.   }
5. }
```

##### Branch code
```js
1. for (var i = 0; i < myArray.length; i++) {
2.   var currentItem = myArray[i];
3.   if (currentItem.length === 3) {
4.     console.log("This is a short word");
5.   }
6. }
```

Git will not automatically merge this code since the original code has been modified on lines 2 and 3. Git cannot make assumptions about which code is correct, so when a merge is attempted, it alerts the developer that there are merge conflicts.

When you get this message, you need to open up the file in your code editor and you'll see something like this.

```js
1. for (var i = 0; i < myArray.length; i++) {
2. <<<<<<<<
3.   if (myArray[i].length === 3) {
4.     console.log("This is a short word");
5. ========
6.   var currentItem = myArray[i];
7.   if (currentItem.length === 3) {
8. >>>>>>>>
9.     console.log("This is a short word");
10.   }
11. }
```

The code between the `<<<<<<<<` decorator and the `========` decorator is the code that currently exists in master. The code between `========` and `>>>>>>>>` is the code that is in the branch being merged. You, and possibly your teammates, need to decide which is the correct code, and then delete the decorators.

Once the code looks good, you will need to add and commit the resolved file.

> **Note:** Sometimes when you commit after you resolve merge conflicts, you'll get thrown into vim with a default merge message. You can just accept the default message and press `:x` and then press the enter key.

# Additional Resources

[Comparing Git Workflows](https://www.atlassian.com/git/tutorials/comparing-workflows)
