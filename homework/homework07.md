1. **What happens to mycp if one or more of the files to be copied
   doesn’t exist? Can you make any suggestions to better handle the situation?**
   
   Our call to `cp` within the `mycp` program realizes that these files do not exist and throws an error.
   I would try adding an if statement within the `for from...` loop to check if the `from` file exists. If it
   does not exist, let the user know and continue to the next file.

2. **What happens to mycp if one of the filenames contains a character
   that has a special meaning to the shell such as ; or |?**
   
   The shell still interprets those special characters—usually breaking proper program execution.

3. **Write a program called mymv that does with the mv command what mycp
   does with the cp command. How many changes did you have to make to
   mycp to produce this new program?**
   
   Basically one change to make the functionality work. I changed the 'cp' call to 'mv'.

4. **Modify mycp to prompt for arguments if none are supplied. A typical
   execution of the modified version should look like this:**
   
   ```
   $ mycp
   Source file name? voucher
   Destination file name? voucher.sv
   ```

   > Make sure that the program allows one or both of the files to be specified with filename substitution characters.
  
   ```sh
   if [ "$numargs" = 0 ] ; then
     printf "What is the source file name? "
     read -r sourceFile

     printf "What is the destination file name? "
     read -r destinationFile

     filelist="$sourceFile"
     to="$destinationFile"
   elif [ "$numargs" -lt 2 -o "$numargs" -gt 2 -a ! -d "$to" ] ; then
     echo "Usage: mycp file1 file2"
     echo "       mycp file(s) dir"
     exit 1
   fi
   ```

5. **Add a -n option to mycp that suppresses the normal check for the
   existence of the destination files.**

6. **Modify mycp to use sed instead of the while loop to process the
   arguments typed on the command line.**

7. **Modify the rem program used by rolo so that if multiple entries are
   found, the program will prompt the user for the entry to be
   removed. Here’s a sample session:**
        
  ```
  $ rolo
  
  ...
  
  Please select one of the above (1-3): 3
  Enter name to be removed: Susan
  More than one match; please select the one to remove:
  Susan Goldberg Remove (y/ n)? n
  Susan Topple Remove (y/ n)? y
  ```

8. **Modify rolo so that the menu is redisplayed after each selection is
   made and processed. To allow the user to get out of this, add
   another selection to the menu to exit from the program.**

9. **What happens to the rolo program if just an Enter is given as the
   name for the add, look up, or remove options?**

10. **Modify lu to use printf to print the name and phone number so that
    they line up in columns for names up to 40 characters in length
    (Hint: use cut –f and the fact that the fields in the phonebook
    are separated by tabs).**
    
