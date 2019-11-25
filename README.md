# HTLW3R GIT Essentials
Small repository to show the absolute basics used at the HTLW3R.
This repository has been created while holding a crashcourse for newcomers to GIT.
The skills tackled in this crashcourse are also covered on https://my.htl3r.skilldisplay.eu/skill/135/29 in case you want to track your progress.
(You need to be registered with the school to use this feature)

## Why would I want to use GIT?
It helps you to travel back in time to recover your code from a state where 

## Are there alternatives? Are they used?
SVN comes to mind (e.g: Ankh with Tortoise), practically you'll want to use GIT however, it is the de facto standard.

## What would you recommend for teams of students?
Give all students permissions to the repository via settings.

In order to keep the master branch as clean as possible and prevent a lot of merging one solution is using feature branches.
If you develop a new feature, start by
- git checkout -b featurename

This creates a new branch on which you can develop your code and make multiple commits. As soon asyou are content with the result you can make a pull request to the master branch. For newbies this should be easiest by using the graphical interface of the webbrowser (switch to the branch, click on the green "create pull request" button)

If you use standard project management techniques like waterfall or scrum you could create a tag for each milestone/sprint by introducing a tag.
- git tag -a "v0.1" -m "Information about the version"

Mind that you can only push to a single tag once. (So make sure your version is in order before pushing) 

## Which are the basic commands and concepts?
- Repository (commit, push, pull)
- git commit -m "[TASK/FIX] Meaningful text in present form"
- .gitignore
- Branch (checkout)
- Tag (add, push to tag)
- Merge

## Resource list
- https://git-scm.com/
- https://github.com

## Linux commands
- cd : change directory
- ls : list all files/directories (-la lists hidden files and user permissions)
- mkdir : directory erstellen
- ~ is the home directory (cd ~)
- touch : creates a new file

## What are the most common starter problems?
- A person creates a new repository on GitHub and decides to include a ReadMe with it - thus a repository and Readme are created. The person however already has different files in a local directory, creates a commit and wants to push said changes. Now there are "unrelated histories", as there are "2 Beginnings" for the repository. You can fix that if you set the flag "allow unrelated histories"
- A person is unable to push their changes, because the remote repository contains work that they don't have. Use "git pull" before pushing your changes
- A person made changes and wants them undone, the files have not yet been added "git checkout . --" (careful, this undos all your local changes which are not yet committed!)
- A person worked for a time and realizes he/she is on the wrong branch: "stash" your changes, change to the correct branch, "unstash" them. https://git-scm.com/book/en/v1/Git-Tools-Stashing
