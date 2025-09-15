# Linux System Adminstration 
Practicing Linux commands using the CLI of GitHub Codesacpes Terminal.

# Using Bash
- Check bash version:
    ```bash
    bash --version
    ```
    - Output:
    ```
    GNU bash, version 5.2.21(1)-release (x86_64-pc-linux-gnu)
    Copyright (C) 2022 Free Software Foundation, Inc.
    License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
    ```

- General Command Syntax:
    - Command => Option(s) => Argument(s)
    ```
    ls -lh /usr/bin
    sort -u users.txt
    grep -i "needle" haystack
    ```
    - Commands: ls, sort, grep
    - Options: -lh, -u, -i "needle"
    - Arguments: /usr/bin, users.txt, haystack
- Shell is case sensitive: "ls" not same as "LS"
    - just list all the files:
    ```bash
    ls
    ```
    - long listing with detailed info
    ```bash
    ls -l
    ```
- Running a wrong command (doesn't exist)
    ```bach
    list
    ```
    - ouput:
    ```bach
    bash: list: command not found
    ```
- Linux Manual pages (The full linus refernce book) command:
    ```bash
    man
    ```
    - output:
    ```
    What manual page do you want?
    For example, try 'man man'.
    ```
    - help with "ls" command:
    ```
    man ls
    ```
    - output:
    ```
    NAME
       ls - list directory contents
    
    SYNOPSIS
       ls [OPTION]... [FILE]...
    
    DESCRIPTION
       List information about the FILEs (the current directory by default).  Sort entries alphabetically if none of -cftuvSUX nor --sort is specified.

    Manual page ls(1) line 1 (press h for help or q to quit)
    ```
    > **NOTE: Press "Q" or "q" to quit the list/output of this command**
- Getting help for all commands, writing the command then --help:
    ```
    ls --help to list the commands
    ```
- See the output page by page using Pipe symbol "|":
    > adding the coptions after "|"
    > ls --help | less
    > **NOTE: Press "Q" or "q" to quit the list/output of this command**
- Getting the full general help:
    ```
    help
    ```
    - ouput:
    ```
    GNU bash, version 5.2.21(1)-release (x86_64-pc-linux-gnu)
    These shell commands are defined internally.  Type `help' to see this list.
    Type `help name' to find out more about the function `name'.
    Use `info bash' to find out more about the shell in general.
    Use `man -k' or `info' to find out more about commands not in this list.

    A star (*) next to a name means that the command is disabled.

    ...etc...
    ```
- Find commands related to a topic​ (searching for specific command) using **paropos**
    - with out specifying any parameters:
    ```
    apropos    
    ```
    - output:
    ```
    apropos what?
    ```
    - specify the topic, example "list:
    ```
    apropos list
    ```
    - example "create":
    ```
    aporpos create
    ```
- Fillter in the output using the "grep"
# Pipes:
Used to connect Linux commands 

- List the files inside a directory "temp:
    - using -l for all files
    - /temp for the folder name
    - * for any file with any number of characters
    - ls -l /temp/*