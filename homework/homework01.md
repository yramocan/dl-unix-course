# Unix Fundamentals Homework #1

1. **Who created Unix? Where and when?**

    - Unix was created by Ken Thompson & Dennis Ritchie at Bell Labs in the 1960s.

2. **Who created Linux? When?**

    - Linus Torvalds created Linux in 1991.

3. **What is an operating system?**

    - An operating system is software that manages hardware/software resources to provide 
    commonly-used services for computer programs.

**Given the following files in your current directory:**

- `feb96`
- `jan12.02`
- `jan19.02`
- `jan26.02`
- `jan5.02`
- `jan95`
- `jan96`
- `jan97`
- `jan98`
- `mar98`
- `memo1`
- `memo10`
- `memo2`
- `memo2.sv`

4. **What would be the output of the following commands?(Note, ranges in globs are guaranteed to work properly only in the POSIX locale, so assume that.)**

    ```sh
    echo *
    echo *[!0-9]
    echo m[a-df-z]*
    echo [A-Z]*
    echo jan*
    echo *.*
    echo ?????
    echo *02
    echo jan?? feb?? mar??
    echo [fjm][ae][bnr]*
    ```
    
    - `echo *` prints all filenames in the current directory to the console.
    - `echo *[!0-9]` prints `memo2.sv` to the console since it is the only filename that doesn't end in a number.
    - `echo m[a-df-z]*` prints the filename `mar98` to the console (or any file that begins with `m` and any letter other than `e`.
    - `echo [A-Z]*` prints `[A-Z]*` to the console since there is not a filename that begins with an uppercased letter.
    - `echo jan*` prints all filenames that begin with `jan`.
    - `echo *.*` prints all filenames in the directory that have a `.` character somewhere in the middle of the name.
    - `echo ?????` prints all 5-character filenames in the directory, as specified by 5 the question marks.
    - `echo *02` prints all filenames in the directory that end in `02`.
    - `echo jan?? feb?? mar??` prints any 5-character filenames which begin with `jan`, `feb`, or `mar`.
    - `echo [fjm][ae][bnr]*` prints all filenames that begin with either `f`, `j`, or `m` followed by `a` or `e` then `b`, `n`, or `r`. As a result, `feb96 jan12.02 jan19.02 jan26.02 jan5.02 jan95 jan96 jan97 jan98 mar98` is printed to the console.

4. **What is the effect of the following:**

    ```sh
    ls | wc -l
    rm ???
    who | wc -l
    mv progs/* /users/steve/backup
    ls *.c | wc -l
    rm *.o
    who | sort
    cd; pwd
    cp memo1 ..
    plotdata 2>errors &
    ```
    
    - `ls | wc -l` prints the number of lines printed from `ls` output (the number of files in the current directory).
    - `rm ???` removes all files with filenames of only 3 characters.
    - `who | wc -l` prints the number of current user sessions. In my case, it printed `2` since I had one session for macOS and one Terminal session open.
    - `mv progs/* /users/steve/backup` moves all files from the `progs/` directory to `/users/steve/backup`.
    - `ls *.c | wc -l` pipes the output of `ls *.c` to `wc -l` and prints the number of lines, or the number of files with filenames ending in `.c`.
    - `rm *.o` removes any files with filenames ending in `.o`.
    - `who | sort` prints the list of current user sessions in alphabetical order.
    - `cd; pwd` changes to the home directory then prints the working (home) directory path.
    - `cp memo1 ..` copies the file named `memo1` to the parent directory (one level above the current directory).
    - `plotdata 2>errors &` redirects the standard error from running `plotdata` to the file `errors`, sends the process to the background, then prints the PID of that process.

> The rest of the exercises in this session involve the provided files
> in the Session 1 directory of the git repository for this
> course. Please clone the repository and navigate to the session1
> directory.

5. **How many files are in the session1 directory?**

    - There are 4 files in `session1/`.

6. **How many directories are in the session1 directory?**

    - There is 1 directory named `dir1/` in `session1/`.

7. **How many characters are in the file session1.md?**

    - There are 13186 characters in `session1.md`.

8. **What commands other than echo are used in the myprogram script?**

    - Excluding `echo`, `ls` and `date` are used in the `myprogram` script.

9. **Write a command to show how many names are in the names file.**

    - `wc -l names`

10. **From dir1 (that is, with dir1 as your working directory), write a
    command to copy file1 to file1_backup.**
    
    - `cp file1 file1_backup`

11. **From dir1 (with dir1 as your working directory), write a command
    to move file3 to dir3.**
    
    - `mv dir2/file3 dir3`

12. **From dir1, write a command to rename file8 to happy_file.**

    - `mv dir3/file8 happy_file`

13. **From dir2, write a command to copy file2 to the working directory.**

    - `cp ../file2 file2`

14. **From dir3, write a command to move file5 to dir1.**

    - `mv ../dir2/file5 ../`

15. **From dir1, write a command to copy all files that start with "f"
    to dir2.**
    
    - `cp f* dir2`

16. **From dir2, write a command to move all files that end in a number
    to dir1.**
    
    - `mv *[0-9] ../`
    
17. **From dir1, write a command to move all files that start with an
    "f" and end with a number from dir2 to dir3.**
    
    - `mv dir2/f*[0-9] dir3/`

18. **From dir1, write a command or series of commands to delete dir2.**

    - `rm -r dir2`

19. **From dir1, write a command or series of commands to create a
    directory in dir3 which is called dir4, which contains another
    directory, dir5.**
    
    - `mkdir -p dir3/dir4/dir5`

20. **From dir3, write a command or series of commands to delete dir3.**

    - `rm -r ../dir3; cd ..`
