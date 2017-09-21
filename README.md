# Bash Guide - A Quick Guide To Learn Bash Scripting


## Table of Contents

1. [Basic Commands](#1-basic-commands)
2. [System Information](#2-system-information)
3. [Process Management](#3-process-management)
4. [Network Operations](#4-network-operations)
5. [Shell Programming](#5-shell-programming)


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

### iv. df

Displays file system disk space usage.

```
df
```

### v. du

Displays the disk usage of files and/or directories.

```
du [options] filename|dirname
du -sh /sbin/file1
```

Options: 
- h - Human readable format (size is displayed in KB, MB, GB)
- a - display all (shows disk space for directories at every level and also individual files)
- s - Suppress or Summarize (only shows total disk space occupied)


### v. top

Displays a dynamic real-time view of a running system with the list of active processes.

```
top
```

### vi. last

Shows listing of last logged in user(s).

```
last
last username
```

### vii. quota

Displays the disk quota (limits) and usage.

```
quota
```


## 3. Process Management

### i. kill

Sends a signal to a process. Commonly used to terminate a process. 

```
kill [signal] PID
```

### ii. killall

Kill all processes by name.


```
killall processname
```

Options: 
- e - Require an exact match for long names
- i - Interactively ask for confirmation before killing
- q - Quiet mode


### iii. fg

Moves a background job to foreground

```
fg [job-id]
```


### iv. bg

Runs a job in the background.

```
bg [job-id]
```


### v. nohup

nohup i.e. No Hangup, runs the given command with hangup signals ignored, so that the command can continue running in the background after you log out.

```
nohup command [arg...]
```


## 4. Network Operations

### i. ping

Used to test if a host is reachable. Sends ICMP ECHO_REQUEST to network host(s). 

``` 
ping [option] host
ping host
ping -t host
```

### ii. dig

Domain information groper, DNS lookup utility.

```
dig domain [options] [query]
```

### iii. w

Shows who is logged on and what they are doing.

```
w [option] [user]
```


## 5. Shell Programming

Shell is a user program or an environment provided for user interaction. Shell is a command language interpreter that executes commands read from the standard input device (keyboard) or from a file.

Shell is not part of system kernel but uses the system kernel to execute programs, create files etc.

Several shells available with Linux including:

- SH (POSIX shell or Bourne shell)
- BASH ( **B**ourne-**A**gain **SH**ell )
- CSH (C SHell)	
- KSH (Korn SHell)	
- TCSH	(TENEX/TOPS C shell)

A shell script begins with a `#!` commonly referred to as shebang, also known as sha-bang, hashbang, pound-bang or hash-pling. 

It's syntax follows: 
```
#!interpreter [optional-arg]

#!/bin/sh
#!/bin/bash
#!/bin/csh -f
```

### Executing a shell script

Syntax:
```
[interpreter] script-name
./script-name
```

On your terminal type:
```
bash scriptA
sh scriptA
./scriptA
```


### i. Variables

Variables in shell programming are typeless (no data types). A valid variable name can consist of characters, numbers, hyphens and underscores. There can be no spaces around the "=" assignment sign: that is `VAR=value` is valid; `VAR = value` is not.

Variables can be accessed by prepending `$` before the `VARIABLE_NAME`.

```
MY_MESSAGE="HELLO!"
echo $MY_MESSAGE
```

### ii. Quotations

There are 4 types of quotes with Shell programming:

| Quote | Name | Description   |
| :-- | ----: | :---: |
| " | Double Quote |  Weak type of quoting, expands variables and command substitutions but not meta-characters  |
| ' | Single Quote | No special characters are expanded |
| ` | Back Quote | Execute everything in between back quotes |
| \ | Backslash | Everything immediately following a backslash will not be executed |
