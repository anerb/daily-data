---
title: Introduction
nav: Intro
topics: Tools, Personal Organization
---

DIDIT (Daily Individual Data Input Tools) is a collection of digital tools to help you personally collect and organize data you care about.

The data is you collect is for your own personal use and stays as private as if you had recorded it manually yourself.

There are two main parts to the organizing your daily data
  1. Convenient ways to capture or input the data (e.g. the price on a purchase you made, or the fact that you took today's pill.)
  2. An accessible place to store the data for you to use however you want.
-------------

## Capturing your data

Capturing data is hard.  Anyone who tells you "Just write down every time you eat a snack." is making the word *just* do a lot of work in that sentence.

Mini apps on your phone are an important part of making recording the moment as simple as possible (but no simpler).

Here are some example mini apps that work with the DIDIT mentality
 - **Spendior** - Record every time you spend money on something.
 - **Selfmore** - Record health data about your self to help you take better care of your self. (Don't be selfless, be selfmore.)
   - Not yet ready - coming soon.
 - **Promistake** - Takes down a record of your promises.  Helps you avoid the mistake of forgetting to keep a promise.
   - Not yet ready - I'm not promising anything.

### Mini app philosophy
The mini apps work for you.  They do not send data to any servers, and they don't make anything up.  This is about helping you with interfaces customized to certain data-entry tasks.  This is not about collecting data for you that aren't inputing yourself.

To meet this philosophy, DIDIT mini apps use email to send the data for off your phone.  By using your email, the apps let you have full control over what gets sent from your phone, and it remains as private as sending an email to yourself.

## Storing the data

For better or worse, email is a basic means of communication that nearly everyone has access to.  DIDIT relies on email as sort of [Pub/Sub](https://en.wikipedia.org/wiki/Publish%E2%80%93subscribe_pattern) system for the world.

Email2Sheet is designed around Google's Apps Script framework to process incoming emails (to a Gmail account) and store their information in a Google Sheet[¹].



[^1] Similar systems could potentially be built around Micorosft's Outlook/Excel or Apple's iCloud Mail/Numbers, and open source projects like Proton Mail/LibreOffice.  For now, Google's Gmail/Sheets is recommended even if you don't regularly use the Google ecosystem.  There are [ways](https://www.freshtechtips.com/2021/11/sync-excel-google-sheet.html) to bring the data into Excel or other formats you may prefer to work with.  As mentioned above, the goal of DIDIT is to collect and reliably store records.  What you do with the data from there is up to you.


### Install Git

[Git](https://git-scm.com/) is a [free](https://www.gnu.org/philosophy/free-sw.en.html), [distributed](https://en.wikipedia.org/wiki/Distributed_version_control) version control system. [GitHub](https://github.com/) is a Git repository hosting service, a place to store and sync your work in the cloud.
Your GitHub project will be under Git version control, so you need the software on your machine. 

- **Windows:** Install [Git for Windows](https://git-scm.com/downloads){:target="_blank" rel="noopener"} using the default options, *except* when setup asks you to choose the default editor used by Git, select "Use the Nano editor by default". This will give you Git, Git Bash, and Git GUI. Git Bash is a terminal that lets you use UNIX style commands and utilities on Windows, and will be used as your default terminal when working with Jekyll.
- **Mac:** Mac systems will require the "Xcode Command Line Tools" installed, so open a terminal (to find your terminal search for "terminal" in your Spotlight), type in the command `xcode-select --install`, and follow the prompts. After the install finishes, try typing `git --version`. If you want a newer version of Git, download the official [Mac git installer](https://git-scm.com/downloads){:target="_blank" rel="noopener"}.
- **Linux:** Install from your distribution's software center or package manager (for Ubuntu `sudo apt install git`).

If you are interested in using a visual GUI application integrated with GitHub, Windows and Mac users should also install [GitHub Desktop](https://desktop.github.com/) using the default options.
You can install GitHub Desktop in addition to other versions of Git.
There are other [GUI apps available](https://git-scm.com/downloads/guis) for managing and visualizing Git repositories, including Linux options.

### Install Ruby

[Ruby](https://www.ruby-lang.org/en/){:target="_blank" rel="noopener"} is a open source programming language popular with web applications.
**_You do not need to know anything about Ruby_**, but you do need it to run Jekyll on your system!

Jekyll requires a Ruby version 2.5.0 or greater.
Below are quick start steps, but you may want to refer to Jekyll's official [installation guides](https://jekyllrb.com/docs/installation/) for tips.

- **Windows:** Use [RubyInstaller for Windows](https://rubyinstaller.org/){:target="_blank" rel="noopener"}.
    - First, [download](https://rubyinstaller.org/downloads/) the suggested stable version "WITH DEVKIT" (as of this writing, Ruby+Devkit 3.1.x (x64)) and double click to install. Use the install defaults, but make sure "Add Ruby executables to your PATH" is checked. On the final step, ensure the box to start the MSYS2 DevKit is checked.
    - Second, the installer will open a terminal window with options to install MSYS2 DevKit components. Choose option 3, "MSYS2 and MINGW development toolchain", or simply press ENTER to install all the necessary dependencies. The installer will proceed through a bunch of steps outputting a bunch of text in the terminal window. *Eventually*, this will conclude and you should see a message with the word `success` in it. If the window doesn't close, press `Enter` again or manually close it. (The installer can be restarted by typing `ridk install` into a command prompt).
- **Mac:** OS X has a version of Ruby installed by default. Check the version with `ruby -v`. If it is > 2.5.0 you can use the system Ruby. However, a newer version can be installed using [Homebrew](https://brew.sh/) or a manager such as [rbenv](https://github.com/rbenv/rbenv). Check the official Jekyll [Mac install docs](https://jekyllrb.com/docs/installation/#macOS) for tips.
- **Linux:** Although many distros come with a system Ruby installed or a repository version, we suggest using a version manager such as [rbenv](https://github.com/rbenv/rbenv) or [RVM](http://rvm.io/). This will ensure you have an up to date Ruby version and a clean environment separated from your system Ruby. You will also need the build tools Make and GCC, on Ubuntu get them with `sudo apt install build-essential`. 

### Install Jekyll

Jekyll is a Gem, a software package installed via Ruby's management system called RubyGems (similar to Python's Pip). 
Open a terminal and type:
`gem install jekyll bundler`

This will take a minute as Gem installs all the dependencies and builds extensions. 

### Install Text Editor

When working with code you should have a good text editor.
Windows notepad does not handle UTF-8 encoding or UNIX line endings that are standard for cross platform applications. 
For basic editing, Windows [Notepad++](https://notepad-plus-plus.org/), Mac TextEdit, or Linux Gedit are sufficient.
However, a more complete code editor will be helpful for managing Jekyll projects.
The current most popular open source cross platform option is [Visual Studio Code](https://code.visualstudio.com/).
