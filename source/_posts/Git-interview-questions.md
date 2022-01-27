---
title: Git interview questions
date: 2022-01-27 15:03:50
tags: [Git, interview]
---

### 1. What is ‘Version Control System’?

it is a program that records any changes to a file or set of data so that it is possible to restore it to a previous version if necessary. This guarantees that everyone on the team is working on the most up-to-date version of the file.

### 2. Differentiate Between Centralized and Distributed Version Control System

![Centralized and Distributed Version Control System](https://cdn.jsdelivr.net/gh/zio7711/blog-pic/20220127151508.png)

Centralized Version Control system:

- It stores all file  versions on a central server.
- No developer has complete copy of the local system's files.
- If the project's central server fails, you will lose all the project's data.

Distributed Version Control system:

- Every developer has a copy of all the code versions on their computer.
- Improves the ability to work offline and eliminates the need for a single backup location.
- Even if the server crashes, there is no danger.



### 3. Explain Git Push and Git Pull

**Git push**: is a command that pushes the contents of a local repository to a remote repository. It runs a push after it has changed a local repo to share the changes with remote team members.

**Git pull**: is a command that pulls changes from a repository and merges them into the local repository. It's made up of two commands: git fetch followed by git merge.

