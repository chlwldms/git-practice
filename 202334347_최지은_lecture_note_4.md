# **About Shell Commands** 

***What is Shell command?***
A shell command is a text-based interface used to interact with the operating system and execute commands.

-------------

 ### *1. About movement for file and directory*
 
 * pwd : shows the current path in a hierarchical directory
    ```sh
    $pwd
    /C/Users/user
    ```
    
 * cd : change directory
    ```sh
    $cd Downloads
    /C/Users/User/Downloads
    ```

* ls : list files and directories
    * ls -l : show detailed information(long format, like Byte count, Date of Creation, file or directory name)
    * ls -lh : same as above, but size in units (byte counts -> KB, GB etc...)
    * ls -la : list all files in the parent of the working directory in long format

* <arguments>
    * . : current directory
    * .. : upper-level directory
    * ~ : home o current user
    * /\[directory name] : absolute path
    * ./\[directory name] : relative path
    * ../\[directory name] : relative path (move upper-level directory and move directory)

\[TIPS !]
"tab" key : Automatocally directory name completion
"up arrow" key : Import the above commands

------------------

### *2.About manipulation for dile and directory* 

* cp : copy files and directories
    * cp -i file1 file2 : copy the contents of "file1" to "file2" while prompting the user for confirmation before overwriting any existing "file2"
    * cp file1 dir1 : copy a file named "file1" to a directory named "dir1"
    * cp -R dir1 dir2 : copy the contents of a directory (dir1) to another directory (dir2) *recursively*

* mv : move files and directories or rename them
    * mv -i file1 file2 : move or rename a file named "file1" to a new name "file2". The "-i" option prompts the user for confirmation before overwriting an existing file with the same name.
    * mv file1 file2 dir1 : move file1 and file2 to the directory dir1
    * mv dir1 dir2 : moves the directory named "dir1" into the directory named "dir2"

* rm : delete files and directories ***permantely and irreversevely !!***
    ```sh
    $ pwd
    /C/Users/User/Downloads
    $ ls
    README.md new_module.py
    $ ls 
    README.md
    ```
    * rm file1 file2 : delete file1 and file2
    * rm -i file1 file2 : remove two files, file1 and file2, with an interactive prompt for confirmation before deletion
    * rm -r dir1 dir2 : directories dir1 and dir2 are deleted along with all of their contents

* mkdir : make a new repository

---------

### *3. Help Command*

* help (command) : display information about the usage and syntax of other commands in a system
* man (command) : displays the manual pages for a specific command
* 



    
