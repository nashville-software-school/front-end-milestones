# The Zen Garden Challenge

## Setup

Run the following command in your terminal:

```bash
mkdir -p ~/workspace/exercises/the-static-web/zen-garden && cd $_
```
> This will create a project folder and cd you into it.

+ Create a new GitHub repository.
+ Once your repository is created, copy the list of commands under **"..or create a new repository on the command line"** by clicking on the clipboard icon.
+ Paste the commands into your terminal. This will create a README.md file, add it, commit it, connect your local repo to GitHub, and set you up to push up the changes. (If the last command, `git push origin master` isn't automatically executed, hit enter/return to run it).

All of your work should be on a branch, NOT on master. To do this, type:

```bash
git checkout -b exercise
touch index.html
touch style.css
mkdir images
```

> You are now ready to work in the `exercise` branch.

## Instructions

Visit http://www.csszengarden.com/ and explore some of the designs.

You will create your own version of the CSS Zen Garden.

Download the HTML and CSS files.  
:paperclip: [HTML](http://www.csszengarden.com/examples/index)  
:paperclip: [CSS](http://www.csszengarden.com/examples/style.css)  

Copy the contents of the HTML file into your `index.html`.  
Copy the contents of the CSS file into your `styles.css`.  

> The only rule: you may only change the CSS; not the HTML.

When your work is complete, add, commit, and push up the branch (`git push origin exercise`). Then submit a pull request on Github.

> :pencil2:  In an effort to keep this project like the Zen Garden website, this exercise does not have a styles folder.
