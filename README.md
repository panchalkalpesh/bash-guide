# Bash Guide - A Quick Guide To Learn Bash Scripting


## Table of Contents

1. [Basic Commands](#1-basic-commands)
2. [System Information](#2-system-information)



## 1. Basic Commands

### i. `ls`
List files and directories. 
```
ls [options]
```

Options: 
- l - long listing format
- a - show all files (including hidden files)


### ii. `cd`

Change current directory (move to another directory)

```
cd directory-path
```

### iii. `cp`

Copies a directory or file to destination

```
cp source destination
```

### iv. `mv`

Moves a source from one path to another. This command is also used to rename directories and files.

```
mv path1 path2
mv filename1 filename2
```

### v. `rm`

Removes a file(s) or directory(s). 

```
rm file1 file2
rm -r directory1
```

Options:
- f - force deletion without any prompt


### vi. `touch`

Create a file. If file already exist, update dates accessed and modified

```
touch filename
```


### vii. `file`

Determine filetype of file(s).

```
file filename
```

Options:
- i - output MIME type strings


### viii. `diff`

Compares files line by line and displays the difference.

```
diff file1 file2
```

### ix. `cat`

Concatenate FILE(s) to standard output. It can be used to display text files on screen, create, copy, merge files.

```
cat [option] file
cat file1 file2 
cat file1 file2 > newmergedfile
cat < file1 > file2 #copy file1 to file2
```


### x. `more`

Displays output one screen at a time. Move to next page by pressing `space` or press `q` to quit.

```
more filename
```


### xi. `less`

Similar to `more` but allows both forward and backward movements. You can also use arrow keys to move one line at a time.

```
less filename
```



## 2. System Information

### i. uname

Prints kernel information on the screen.

```
uname [option]
uname -a
```


### ii. ps

Lists your running processes & their status.

```
ps [option]
ps -a
ps -u user
```

### iii. jobs

Lists the jobs running in the background along with the job number.

```
jobs
```
