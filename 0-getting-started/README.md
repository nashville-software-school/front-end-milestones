# Hardware

Up until now, you didn't have the power to destroy your machine, but within the first two weeks of attending Nashville Software School you will have that power. Go buy a backup drive RIGHT NOW and start backing up your entire hard drive.

**Seriously, right now!**

# Things you need to install

## Everyone

### Create a Github account

Github is the primary site that software developers throughout the world use to store their code, and share it with other developers. Visit the [sign up page](https://github.com/join) and create your own, free account.

### Google Chrome

[Google Chrome](https://www.google.com/chrome/browser/desktop/index.html) is the most popular browser for web developers because of the powerful tools it provides to test code, manipulate documents, and measure performance.

### Sublime Text

Visit the [Sublime Text](http://www.sublimetext.com/3) website and click the link that corresponds to your operating system. Then install once the download is complete.

Install the Sublime Text [package control](https://packagecontrol.io/installation) which, in turn, allows you to easily install and manage tons of really cool add-ons for customizing your Sublime editor.

Read [this excellent introduction](https://scotch.io/bar-talk/best-of-sublime-text-3-features-plugins-and-settings) to getting the very most out of Sublime Text. These tips will make coding more enjoyable and increase your speed.

### Install Slack

Do not use the browser-based interface for Slack. Download and use the client. Let us know if you did not get an invitation to the Nashville Software School Slack organization, and we'll send you one immediately.

### Create Codepen account

Visit the [Codepen sign up page](https://codepen.io/signup), and scroll all the way to the bottom to sign up for a free plan. If you like, you can click the "Use info from Github" button when creating your account.

## Windows users

###Git powershell

Visit the [Git powershell](http://www.git-scm.com/downloads) download page click the "Download for Windows" button, and once complete, install the software. Powershell is a command line utility that allows you to run most Unix command inside a Windows environment. This will help you have the same vernacular as the rest of the class, since having a *nix environment is preferred and is how the class is taught.

Git is a program that allows software developers to efficiently manage how their code is versioned, shared, and archived. You will be learning how to use it during class.

###Chocolatey package manager (*optional*)

Windows, like OSX, does not have a built in package manager (a fancy term for a piece of software that lets you easily install other software that you need as a developer). There will be times, many weeks into class, as you gain confidence and skill, that you will want to use a package manager. Therefore, if you feel up to the task - meaning, you were able to install all the required software easily - you may want to install Chocolately.

Here's the [official page](https://chocolatey.org/), but it's instructions are written to an audience of existing software developers and may be confusing for a layperson. Here's the basic instructions.

1. Press your Windows key.
1. Type `cmd` into the search box.
1. You'll see a black box as the first search result named `cmd`.
1. Right click that icon and select the "Run as administrator" option. This opens up the _**Windows Command Line**_.
1. When that starts, copy the following command with Ctrl+C, and once that's done paste it into the command line by right-clicking anywhere in that window.
  `@powershell -NoProfile -ExecutionPolicy Bypass -Command "iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))" && SET PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin`

# Homebrew for Mac users

Visit the [homebrew home page](http://brew.sh/) and follow the single instruction there to get it installed.

