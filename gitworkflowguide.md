---
layout: resource
title: Git Workflow Guide
permalink: /resources/git/
published: false
---
This is a crash-course guide to being productive with Git. This guide assumes you are in a UNIX-like environment
(including WSL, Git-Bash, and Cygwin on Windows). The `$` symbol at the beginning of command lines denotes your 
terminal prompt and should not be included with any commands if you copy and paste.

## Contents
* Contents will go here
{:toc}

## The Most Important Rule
As a general rule, you should never commit directly to the master branch, especially if you're working on a
project with a group. Best practice dictates you should create a new branch off of master, make your commits to the new
branch, then merge the new branch back into master.

## Creating a New Repository
First, create a new directory that the git repository will live in on your machine:

`$ mkdir myproject`

`$ cd myproject`

Inside of your project's directory, we need to tell Git to treat this directory as a repository:

`$ git init`

## Making Commits


## Branching


## Appendix
### Removing Files from Staged for Commit


### Undoing a Commit
Sometimes I work on projects where we only ever commit to master. In
these cases it is extremely important to run a `git pull` before committing any work. Every now and then, though, I
forget. This can be solved by running:

``

### .gitignore
