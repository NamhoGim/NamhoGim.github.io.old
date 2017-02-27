# git summary 

All feature and contents from “Codecademy”. Summary by NH

**The Git workflow consists of editing files in the working directory, adding files to the staging area, and saving changes to a Git repository. **

## Git work flow

![Screen Shot 2016-08-19 at 16.12.16.png](https://lh5.googleusercontent.com/V_SVXBY_6BUwHcSzpFGF3AVNQi_mq0PKGHKkCGLl3eoxu8HT5DIxhwRRbihbWgDvbnk3i30zfMIrPT5lMN3KDV4B_kXxLk0l2oCo5dXDSauxzu6S3MI6QcjkcKOMeBW-LkUh1sBd)

A Working Directory: where you'll be doing all the work: creating, editing, deleting and organizing filesA Staging Area: where you'll list changes you make to the working directory

A Repository: where Git permanently stores those changes as different versions of the project

## Basic Commands 

- git init : git initialization, creates a new Git repository, The command sets up all the tools Git needs to begin tracking changes made to the project.
- git status : check the status of those changes
- git add : add file git tracking list git add filename_1 filename_2
- git diff : check the differences between the working directory and the staging area
- git commit : A commit permanently stores changes from the staging area inside the repository.
- git log : Commits are stored chronologically in the repository and can be viewed with this comand.
- git show HEAD : display everything the git log command displays for the HEAD commit, plus all the file changes that were committed.
- git checkout HEAD filename : Discards changes in the working directory. will restore the file in your working directory to look exactly as it did when you last made a commit.git reset HEAD filename : unstage file from the staging area.
- git reset commit_SHA : Git enables you to rewind to the part before you made the wrong turn and create a new destiny for the project.

## Reset

![Screen Shot 2016-08-20 at 00.47.59.png](https://lh6.googleusercontent.com/g7z8lohtUVTww1kMF_p68iuA4B1SKY235p8fhRHJcQMM6jl86j9vOOUqxzV8lSauysaHrL1cZBJ5lo63I8mBPTk8IXrc_SPTGkd7WkEttsqo0e8bYuzJ2IDhnlea7L-FTGrvy6wK)      Before resetHEAD is at the most recent commit

After resettingHEAD goes to a previously made commit of your choiceThe gray commits are no longer part of your project

You have in essence rewinded the project's history	

## Git Branching

![Screen Shot 2016-08-20 at 00.55.23.png](https://lh6.googleusercontent.com/WldPYQp41tQyXBGUw4uqLfXGoRUOvFUIdKadC-eSv-8LCYKV4gfjUwIquU6FdAnzUwhs28Rv6mdAt7iUxWwbUZVRqCD2t1ZYFVjMgxkooH9-TUoEc8g0dtdt37hRQHE80OS8b4k3)

The circles are commits, and together form the Git project's commit history. New Branch is a different version of the Git project. It contains commits from Master but also has commits that Master does not have.git branch : which branch am i on? If you want to see all of  branch list type git branch git branch new_branch : make new branch identical to HEADgit checkout new_branch : switch to the newly created branch       Mergegit merge branch_name : merge branch into master. Before you merge you should change branch to your master by using command git checkout master.	In case of conflict : 	

<<<<<<< HEAD	master version of line	=======	

'>>>>>>>>>'fencing version of line	



 branch_name	Delete content except you want before you add and commit.git branch -d branch_name : delete specified branch from Git project.Git Teamwork (Using remote repository)git clone remote_location clone_name : clone remote repository into your own local directory. remote_location tells Git where to go to find the remote. This could be a web address, or a filepath.clone_name is the name you give to the directory in which Git will clone the repository.git remote -v : show list of git’s projects remote repository.Git lists the name of the remote, origin, as well as its location. Git automatically names this remote origin, because it refers to the remote repository of origin. However, it is possible to safely change its name. The remote is listed twice: once for (fetch) and once for (push).git fetch : brings those changes onto what's called a remote branch.git push origin your_branch_name : push your branch up to remote.git pull : Downloads bookmark history and incorporates changes.