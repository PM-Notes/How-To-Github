# How-To-Github

> **Git** is a free and efficient open source version control system created by Linus Torvalds in 2005. 

> **GitHub** was crated in 2008 and is simply an web-based hosting service specifically for Git repositories.

## Background

Git simplified collaborating on projects by giving team members the ability to work on files offline, and easily merge changes with the master branch of a project. 

This allowed multiple people to work on the same files at the same time, any suggested changes can be reviewed, before being pushed into the master branch. 

Git repositories (storage locations) could be saved locally on ones computer, or on a central server and shared amongst teams within an organisation.

Git doesn't care about what the contents of a file is, or its file type, it only cares about the differences between different versions of the same file, so it can keep track of them.  

So Git is not just for code development, its for tracking and collaboration of any type of file, from a simple How To document to complex architectural drawings. 

## Why GitHub?

**GitHub** makes it simple for not only people within the same organisation to collaborate, but anyone anywhere in the world.  Team members dont need to be on the same network to be able to collaborate. Changes can be created in their own branches, and merged into the master version when reviewed and approved. And of course we dont need to manage servers, storage, backups or the app.  There is also a very large community, so there is a lot of inspiration and support.

Nowadays, Git is synonymous with GitHub. 

## Types of GitHub

Acc Type | Differences
------------|---------------------------------------------
GitHub Free | Less granular permissions and features.
GitHub Enterprise | More granular permissions and features, advanced reviewing.

## How to Access & Manage Git Repositories

There are 3 ways to access Git when collaborating, creating or managing files and repositories: 

* Via command line
* Via a browser at [github.com](https://github.com) 
* Via the [PC/MAC app](https://desktop.github.com/)

All 3 do a similar thing.  Generally speaking you will use a combination of the CLI and webUI.  You will need to go to the website to create the repository and obtain its unique URL, then usually will use the command line to manage the repository and files. Becoming familiar with the Command Line and Browser is essential, the app is not.

## How do I start?

The **GutHub** [Online Help](https://help.github.com/) is the best reference for beginners and advanced users.  But if you want to get stuck in before you start to reference the help files, we will be doing the following in this article:

* Create a GitHub.com account
* Create a repository in the GitHub.com WebUI
* Install Git
* From ClI, clone the repository so the folder and file is downloaded to our computer.
* Edit the README.md [markdown](https://guides.github.com/features/mastering-markdown/) file that was automatically created with the new repository, then synchronise (push) the changes back to GitHub.com
* Create a new file and synchronise changes back to GitHub.com

## Parlance

Git | Explanation
------------|---------------------------------------------
repository| A folder for files relating to a particular project.
clone| Download a copy of a repository from GitHub to your local computer.
commit| Save changes to files into a staging before pushing back to GitHub.
push | Synchronise the changes from the staging area to GitHub.
branch | Used to isolate development work without affecting other branches in the repository.
merge | Merge a branch into the master file(s)

## Armed with Info!

Now we should have a reasonable understanding on Git, so its probably a good time to put some of this into practice.

### Create a Github Account

Create a GitHub account so that you can create and manage repositories.  With an account you can also watch other peoples repositories for updates, and follow particular members who might inspire you:

[Sign up for Github](https://github.com)

When you log in to GitHub, click on the disclosure icon neat your profile picture (top right) and select **Your Repositories**

1. To create a repository, click on **New**
2. Enter a repository name (or use the suggestion shown!) and optionally enter a description.
3. Set the repository to Public or Private.
4. Tick **Initialize this repository with a README**
5. Leave the two dropdown boxes as **none**
6. Click **Create Repository**
7. Click on **Clone or Download** and click to copy the web URL.

For Example: *https://github.com/NetDevNotes/How-To-Github.git*

## Now for some CLI action!

Now we have created our GitHub account we need to install Git on our local computer, configure Git with our new account details and password, then clone the repository which is currently only in GitHub and houses only a single README.md file in it.  The README.md that was created in step 4 above.

### Install Git

Download and install from [Git](https://git-scm.com/)

You can if you like also install the Desktop App, but at this stage lets not worry about that.  The Desktop app also installs Git command line tools, but in a slightly different way, so lets keep it old-skool and use the above link.

#### Note - I dont want to go into details on installation as it would make this article even larger and there are plenty of articles online to help.

## Setup Git

Once installed, we need to link our local Git to GitHub:

1. Open Terminal (or zSH!)
2. Set your Git username (this is a global setting, and username can be set on a per repository also)

`scripts|master⚡ ⇒ git config --global user.name "NetDevNotes"`

3. Confirm username is set:

```
scripts|master⚡ ⇒ git config --global user.name
NetDevNotes
```

4. Set your commit email address: 

```
scripts|master⚡ ⇒ git config --global user.email "nico@nwten.net"
scripts|master⚡ ⇒ git config --global user.email
nico@nwten.net
```

5. If this hasnt been done automatically, we need to check that we have [Set Commit Email Address on GitHub](https://help.github.com/articles/setting-your-commit-email-address-on-github/)

## At Last!  Clone the repository

So we created the repositoty in the GitHub cloud, setup our local copy of Git and now we would like to download a copy of the files located in HitHub down to our local PC.  This might be to view or to edit the files, and possibly send the edited files back up to GitHub for review or to merge into the master stream.

#### Note - As you can see from my path below, I am working in my home directory under a /scrips folder I created:

```
scripts|master⚡ ⇒ pwd
/Users/nico/scripts
```
```
scripts|master⚡ ⇒ git clone https://github.com/NetDevNotes/How-To-Github.git
Cloning into 'How-To-Github'...
remote: Enumerating objects: 147, done.
remote: Counting objects: 100% (147/147), done.
remote: Compressing objects: 100% (108/108), done.
remote: Total 147 (delta 46), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (147/147), 32.81 KiB | 129.00 KiB/s, done.
Resolving deltas: 100% (46/46), done.
```

# Confirm the repository was downlaoded:

```
scripts|master⚡ ⇒ ls -la | grep How-To-Github
drwxr-xr-x   5 nico  staff   170 16 Feb 15:06 How-To-Github
```

# Change to the new repository folder 

At this stage there is the folder, the .git folder and the README.md. But we have successfully cloned the repo **smile**

```
scripts|master⚡ ⇒ cd How-To-Github
How-To-Github|master ⇒ ls -la
drwxr-xr-x   5 nico  staff   170 16 Feb 15:06 .
drwxr-xr-x   9 nico  staff   306 16 Feb 15:06 ..
drwxr-xr-x  13 nico  staff   442 16 Feb 15:43 .git
-rw-r--r--   1 nico  staff  5757 16 Feb 15:06 README.md
How-To-Github|master ⇒ pwd
/Users/nico/scripts/How-To-Github
```






