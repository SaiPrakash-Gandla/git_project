Version Controlling
=======================
This is the process of maintaining multiple versions of the code
All the team members upload their code(check in) into the remote
version controlling system. The VCS accepts the code uploads from 
multiple team members and integrates it so that when the other
team members download the code they will be able to see the entire
work down by the team

VCS's also preserve older and later versions of the code so that
at any time we can switch between which ever version we want

VCS's also keep a track of who is making what kind of changes

======================================================================

VCS's are categorised into 2 types
1 Centralised version controlling
2 Distributed version controlling

Centralised Version controlling
-----------------------------------
Here we have a remote server(code repository) into which all the team 
members check in the code and all the features of version controlling
are implemented in this remote server

 Distributed version controlling
-------------------------------------
Here we have a local repository installed on every team members machines
where version controlling happens at the level of individual team members
form where it is uploaded into a remote server where version controlling 
happens for the entire team

====================================================================
Setting up git on Windows
-------------------------------
1 Download git from
  https://git-scm.com/downloads

2 Install it

3 Open gitbash and execute the git commands

======================================================================
Setting up git in ubuntu linux servers
--------------------------------------------
1 Update the apt repository
  sudo apt-get update

2 Install git
  sudo apt-get install -y git

----------------------------------------------------------------------
Configuring user and email globally for all users on a system
git config --global user.name "saiprakash"
git config --global user.email "gandla.saiprakash@gmail.com"

-----------------------------------------------------------------------
On the local machine git uses three sections
1 Working directory
2 Stagging Area
3 Local repository

Working directory is the location where all the code is created
Initially all the files present here are called as untracked files

Stagging area is the location where file indexing happens and it 
is the buffer area of git and the files are called as indexed files

Local repository is where version controlling happens and the files
are called as commited files
=========================================================================
Branching in Git
========================
This is a feature of git using which we can create seperate branches
for different functionalites and later merge them with the main branch
also known as the master branch. This will help in creating the code in
an uncluttered way

1 To see the list of local branches
  git branch

2 To see the list all branches local and remote
  git branch -a

3 To create a branch
  git branch branch_name

4 To move into a branch
  git checkout branch_name

5 To create a branch and also move into it
  git checkout -b branch_name

6 To merge a branch
  git merge branch_name

7 To delete a branch that is merged
  git branch -d branch_name 
  This is also called as soft delete

8 To delete a branch that is not merged
  git branch -D branch_name
  This is also known as hard delete

============================================================================
Note: Whenever a branch is create whatever is the commit history of the 
parent branch will be copied into the new branch

Note: Irrespective of, on which branch a file is created or modified git only
considers form which branch it is commited and the file belongs to that
commited branch only.

============================================================================

Working on the Github
=========================
This is the remote repository into which the code is uploaded and
this process is called as checkin

1 Singup for a github account
2 Signin into that account
3 Click on + on top right corner
4 Click on New repository
5 Enter some repository name
6 Select Public or Private
7 Click on Create repository
8 Go to Push an existing repository from command line and copy paste
  the commands
  Enter username and password of github


==========================================================================
Downloading the code from the remote github
===============================================
This can be done in three ways 
git clone
git fetch
git pull

=============================================================
git clone
===============
This will download all the code from the remote repository
into the local repository and it is generally used only once
when all the team members want a copy of the same code

Syntax: git clone remote_git_repo_url

git fetch
==================
This will download only the modified files but it will place
them on a seperate branch called as "remote branch",we can go into
this remote branch check if the modificatios are accpetable and then
merge it with the main branch

1 Open the github
2 Go to the repository that we uploaded
3 Select a file and edit it--->Click on commit changes
4 Open git bash
5 git fetch
6 To see the name of remote branch
  git branch -a
7 To switch into this branch
  git checkout branch_name_from_step6
8 View the modified file
  cat filename
9 If these modifications are ok then merge with main branch
  git checkout main
  git merge branch_name_from_step6


=====================================================================
git pull
===================
This will download only the modified files and merge them with
our local branches
1 Open the github
2 Go to the repository that we uploaded
3 Select a file and edit it--->Click on commit changes
4 Open git bash
5 git pull
  We can see the modified files on the main branch


======================================================================
