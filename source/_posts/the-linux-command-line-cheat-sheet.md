---
title: The Linux Command Line Cheat Sheet
date: 2022-12-05 10:41:24
tags: [linux, docker]
categories: [linux, docker]
banner_img: https://dogefs.s3.ladydaily.com/~/source/unsplash/photo-1518432031352-d6fc5c10da5a?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=774&q=80
index_img: https://dogefs.s3.ladydaily.com/~/source/unsplash/photo-1518432031352-d6fc5c10da5a?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=774&q=80
---

## Managing packages
```bash
apt update
apt list
apt install nano
apt remove nano
```

## Navigating the file system

```bash
pwd         # to print the working directory
ls          # to list the files and directories
ls -l       # to print a long list
cd /        # to go to the root directory
cd bin      # to go to the bin directory
cd ..       # to go one level up
cd ~        # to go to the home directory
```

## Manipulating files and directories
```bash
mkdir test                  # to create the test directory
mv test docker              # to rename a directory
touch file.txt              # to create file.txt
mv file.txt hello.txt       # to rename a file
rm hello.txt                # to remove a file
rm -r docker                # to recursively remove a directory
```

## Editing and viewing files
```bash
nano file.txt               # to edit file.txt
cat file.txt                # to view file.txt
less file.txt               # to view with scrolling capabilities
head file.txt               # to view the first 10 lines
head -n 5 file.txt          # to view the first 5 lines
tail file.txt               # to view the last 10 lines
tail -n 5 file.txt          # to view the last 5 lines
```
## Searching for text
```bash
grep hello file.txt         # to search for hello in file.txt
grep -i hello file.txt      # case-insensitive search
grep -i hello file*.txt     # to search in files with a pattern
grep -i -r hello .          # to search in the current directory
```

## Finding files and directories
```bash
find                  # to list all files and directories
find -type d          # to list directories only
find -type f          # to list files only
find -name “f*”       # to filter by name using a pattern
```
## Managing environment variables
```bash
printenv            # to list all variables and their value
printenv PATH       # to view the value of PATH
echo $PATH          # to view the value of PATH
export name=bob     # to set a variable in the current session
```

## Managing processes
```bash
ps           # to list the running processes
kill 37      # to kill the process with ID 37
```

## Managing users and groups
```bash
useradd -m john     # to create a user with a home directory
adduser john        # to add a user interactively
usermod             # to modify a user
userdel             # to delete a user
groupadd devs       # to create a group
groups john         # to view the groups for john
groupmod            # to modify a group
groupdel            # to delete a group
```

## File permission
```bash
chmod u+x deploy.sh     # give the owning user execute permission
chmod g+x deploy.sh     # give the owning group execute permission
chmod o+x deploy.sh     # give everyone else execute permission
chmod ug+x deploy.sh    # to give the owning user and group execute permission
chmod ug-x deploy.sh    # to remove the execute permission from the owning user and grou
```