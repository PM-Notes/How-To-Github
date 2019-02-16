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
* From Cli, clone the repository so the folder and file is downloaded to our computer.
* Edit the README.md [markdown](https://guides.github.com/features/mastering-markdown/) file that was automatically created with the new repository, then synchronise (push) the changes back to GitHub.com
* Create a new file and synchronise changes back to GitHub.com

## Parlance

Git | Explaination
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

When you log in to GitHub, click on the Profile Pictures disclosure icon and select **Your Repositories**

1.To create a repository, click on **New**
2. Enter a repository name (or use the suggestion shown!) and optionally enter a description.
3. Set the repository to Public or Private.
4. Tick **Initialize this repository with a README**
5. Leave the two dropdown boxes as **none**
6. Click **Create Repository**
7. Click on **Clone or Download** and click to copy the web URL.

For Example 'https://github.com/NetDevNotes/How-To-Github.git'









