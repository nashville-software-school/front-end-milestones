# Creating an Alias for Sublime Text
[What is an alias?](#what-is-an-alias)  
[Will this make my life better?](#will-this-make-my-life-better)  
[Instructions](#instructions)  

## What is an alias?
An alias is simply an abbreviation for a command. Creating an alias can help increase your productivity (Steve has a number of them set up to shorten the amount of characters he needs to type to execute common Git commands) or even to protect yourself from terrible mistakes (i.e. requiring confirmation before removing files).

## Will this make my life better?
Yes.

The alias we're going to set up will allow us to navigate to a directory and simply type `subl .` to open all of the contents of the directory in Sublime Text. Additionally, we could type `subl <FILE_NAME>` to open a specific file.

## Instructions:
  [Windows (Git-Bash)](#windows--git-bash-version)  
  [macOS](#macos-version)  
  [Linux / Ubuntu](#linux--ubuntu-version)

### Windows / Git-Bash Version
1. Open Git-Bash, make sure your working directory is your home directory. If you type `pwd`, you should see something like `/c/Users/yourusernamehere` .
2. Create a file named `.bash_profile` in this directory and open this file in Sublime Text.
3. Paste the following in that file : `alias subl='C:/Program\ Files/Sublime\ Text\ 3/sublime_text.exe'` Note: This file path is where Sublime Text is typically installed by default. If you've changed this, you'll have to edit the path to point wherever sublime_text.exe is installed on your machine.
4. Save this file and exit Git-Bash, restart Git-Bash
5. Navigate to an exercise directory you want to open in Sublime Text and type `subl .` -- This should open the entire directory in Sublime Text.

### macOS Version
### Linux / Ubuntu Version