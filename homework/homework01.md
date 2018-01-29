# Unix Fundamentals Homework #1

1. **Who created Unix? Where and when?**

    - Unix was created by Ken Thompson & Dennis Ritchie at Bell Labs in the 1960s.

2. **Who created Linux? When?**

    - Linus Torvalds created Linux in 1991.

3. **What is an operating system?**

    - An operating system is software that manages hardware/software resources to provide 
    commonly-used services for computer programs.

4. **Do the two exercises at the end of Chapter 2 in the textbook**

    - **TODO**

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
