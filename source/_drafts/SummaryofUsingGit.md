title: "Summary of Using Git"
date: 2015-04-27 18:20:08
tags: [Summary, Notes, Git]
---

## Introduction

I've been use git for several times, starting from using GUI apps such as SourceTree or Tower on OS X. It works quite well, simple and straitforward. However, since I don't have much more experience on complicate project, only familiar with basic concept of commit, checkout, branch and merge. Most of these are well done by these GUI application.

When I switch to Linux in work, I have to learn more about git, especially for the command line usage.

## Branchs and Checkout

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


