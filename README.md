# Git Commands

## git init

```
git init [repository name]
```
This command is used to start a new repository. 

> It will create a .git directory under the working directory. All git related changes will save here.

```
jisjo@my-lappy:~$ git init
Initialized empty Git repository in /home/jisjo/Documents/git/day-3/.git/
```

----



## git config
```
git config –global user.name “[name]” 
git config –global user.email “[email address]”  
```
> the changes will save under .git/config 


This command sets the author name and email address respectively to be used with your commits.

----


## git clone
```
git clone [url]  
```
This command is used to obtain a repository from an existing URL.

----

## git add

```
git add [file]  
```

This command adds a file to the staging area.

```
jisjo@my-lappy:~/$ echo "i am linux" > linux.txt
jisjo@my-lappy:~/$ ll
total 16
drwxrwxr-x 3 jisjo jisjo 4096 Jan 17 08:10 ./
drwxrwxr-x 3 jisjo jisjo 4096 Jan 17 08:07 ../
drwxrwxr-x 7 jisjo jisjo 4096 Jan 17 08:08 .git/
-rw-rw-r-- 1 jisjo jisjo   11 Jan 17 08:10 linux.txt

jisjo@my-lappy:~/$ md5sum linux.txt 
7458e547a834b366899bc26a70506a0e  linux.txt

jisjo@my-lappy:~/$ tree .git/
.git/
├── branches
├── config
├── description
├── HEAD
├── index
├── info
│   └── exclude
├── objects
│   ├── 8e
│   │   └── 491bf8546cdf6239b87caa4f8e47d5e55e4e57
│   ├── info
│   └── pack
└── refs
    ├── heads
    └── tags


```




>  **git add** will create a checksum (md5) value of the content of a text file and it will create a directory under object with named chercksum value. 

```
# echo "i am linux" > linux.txt
# git add linux.txt 
```
