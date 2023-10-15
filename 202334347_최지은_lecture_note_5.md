# **About Shell Commands 2**

### ***1. I / O Redirection***
1.  Standard Output
    :outputting the result of the command being executed on the screen
* Using ">", output can be stored and created in a file
* Commsnd "cat" displays the content of a text file
    ```sh
    $ ls -lh
    total 16k
    -rw-rw-r-- 1 gini 197121  0 Sep 16 2022 README.md
    -rw-rw-r-- 1 gini 197121 23 Nov 13 2022 hello_world
    $ ls -lh > file_list.txt
    $ cat file_list.txt
    total 16k
     -rw-rw-r-- 1 gini 197121  0 Sep 16 2022 README.md
    -rw-rw-r-- 1 gini 197121 23 Nov 13 2022 hello_world
    ```
* Using ">>" appends output to an existing file or create and write to a new file
    ```sh
    $ ls -lh >> file_list.txt
    $ cat file_list.txt
    total 16k
     -rw-rw-r-- 1 gini 197121  0 Sep 16 2022 README.md
    -rw-rw-r-- 1 gini 197121 23 Nov 13 2022 hello_world
    total 20k
     -rw-rw-r-- 1 gini 197121  0 Sep 16 2022 README.md
    -rw-rw-r-- 1 gini 197121 23 Nov 13 2022 hello_world
    ```  
    
2. Standard Input
: Indicate the data that the user enters. It usually accepts input from the keyboard.
* using "<" can redirect input from a file
* You can mix"<" and ">" together in a single line
    ```sh
    $ cat word.txt
    school
    class
    home
    new
    $ sort < word.txt > sorted_words.txt
    $ cat sorted_words.txt
    class
    home
    new
    school
    ``` 
--------

### ***2. various shell command***
* Piplines "|"
    * Forward the output of the previous command to the input of the subsequent command
    * How to use ? : command 1 | command 2 | command 3 | ...
    ```sh
    $ ls -lh | less    #Screen transition / Create a new screen
    ```
    ```sh
    ls | wc -l       # Check the number of files
    ```
* Expansion
: Special characters expand its meaning when given to shell commands
    * echo print out the text
    :Text output as it is when inputting text
    * echo *
    : Tell me the file currently in the directory
    * echo ~
    : Tell the current user's home directory
* Backslah (escape word)
    * it can be used to ignore line change in command, to enter a long command in pultiple lines (Useful when the screen is small)
    ```sh
    $ ls -l \
    > --reverse \        # option full name -> Useful for Scripting
    > --human-readable
    total 16k
    -rw-rw-r-- 1 gini 197121  0 Sep 16 2022 README.md
    -rw-rw-r-- 1 gini 197121 23 Nov 13 2022 hello_world
    ```
    
------------
### ***3. Permissions***
1. About Permission
ex ) -rwxrwxrwx
* FIle type
    * "-" : indicate regular file 
    * "d" : indicate directory
* first rwx
    * Read, write, and execute permissions for **the file owner**
* second rwx
    * Read, write, and execute permissions for **the group owner** of the file
* third rwx
    * Read, write, and execute permissions for **all other users**

2. Chainging Permissions
* chmod : change permissions
    ```sh
    [me@linuxbox me]$ chmod 600 some_file     # numbers like 600 used to set permissions for files or directories
    ```
    |permissions|binary|decimal|
    |---|---|---|
    |rwx rwx rwx|111 111 111|777|
    |rw- rw- rw-|110 110 110|666|
    |rwx --- ---|111 000 000|700|
    |...|...|...|

-------

### ***4.Shell Script*** 
**How to open shell script?**
```sh
$ nano myscript.sh
```

<In scipt file>
```sh
#!/bin/bash

echo "Hello Shell Script!"
```
* #!/bin/bash
: pecifying the type of shell to use in the shell script. In this case, it means using /bin/bash.