title: "Summary of Using Git"
date: 2015-04-27 18:20:08
tags:
---


## Introduction

I've been use git for several times, starting from using GUI apps such as SourceTree or Tower on OS X. It works quite well, simple and strait forward. However, since I don't have much more experience on complicate project, only familiar with basic concept of commit, checkout, branch and merge. Most of these are well done by these GUI application.

When I switch to Linux in work, I have to learn more about git, especially for the command line usage.

## Branches and Checkout

`git merge` and `git rebase` are two commands mainly used to put the changes from a branch to anther. For the difference between `merge` and `rebase`, there is a nicely written documents made by Atlassian.

Normally the use command `git log` will show something like:


    commit 7e05d686e0382446a0319ea33d60edaf51116aeb
    Author: tbsaunde <tbsaunde@138bc75d-0d04-0410-961f-82ee72b054a4>
    Date:   Thu Apr 30 02:08:05 2015 +0000

        fixup libobjc's usage of PCC_BITFIELD_TYPE_MATTERS

        libobjc/ChangeLog:

            * encoding.c (objc_layout_structure_next_member): check value of
            PCC_BITFIELD_TYPE_MATTERS instead of if it is defined.

        git-svn-id: svn+ssh://gcc.gnu.org/svn/gcc/trunk@222605 138bc75d-0d04-0410-961f-82ee72b054a4


or to simply it, use `git log --oneline`:

    7e05d68 fixup libobjc's usage of PCC_BITFIELD_TYPE_MATTERS

It is possible to create a branch using specific commit: `git checkout -b <branch_name> 7e05d68`

To switch between different branches, uses `git checkout <branch_name>` will be enough.

## Stage Commit & Clean
Stage and Commit are used to record the changes in the git repo. 
`git add .` or `git add -A` seems to be identical: to stage the changes.
`git commit` will normally start vi to allow user type the commit message. If the commit message will be short, use `git commit -m '<commit message>'`

Some time we want to remove some untracked files, the `git clean` will be very helpful. Some time also can use `git rm` to manually specify the file to be removed. In addition, “.gitignore” is another way to ignore the files. 

## Status
Use `git status` will show some brief information about the status of current git repo. It will be a good habit to use this command before some important command, such as pull, commit, merge. 

## Remote
The remote repo are quite useful when collaborate with other or using website such as Github. 

A quite useful workflow is that fork some repo from Github, then add the original repo as a upstream remote in the local repo, regularly pull the newest changes into local, so it will be more easier to deal with conflicts and track the upstream progress. 

Commands include: 
- `git remote -v` list the remote repo
- `git remote add <..>` add a remote repo
- `git remote remove` remove a remote repo
- `git push -u | --set-upstream` will allow a branch to track the remote branch.

## Submodules
If want to use other git repo inside a repo, the submodules need to be used to avoid the conflicts between two repos. 

I’m not very familiar with submodule, thus this part will be completed later. 

## More command:
Some commands such as `git stash`, `git tag`, I don’t use them often, so they will also be introduced when I understand what they can do and how to use them. 
