# Bash Guide - A Quick Guide To Learn Bash Scripting


## Table of Contents

1. Basic Commands



## 1. Basic Commands

### i. `ls`
List files and directories. 
```
ls [options]
```

Options: 
l - long listing format
a - show all files (including hidden files)


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
f - force deletion without any prompt


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
i - output MIME type strings


### viii. `diff`

Compares files line by line and displays the difference.

```
diff file1 file2
```

