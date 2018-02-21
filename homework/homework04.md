 1. **Which of the following are valid variable names?**

    - `XxXxXx _` INVALID. Cannot contain a space.
    - `12345` INVALID. Cannot begin with a number.
    - `HOMEDIR` VALID.
    - `file.name` INVALID. Cannot contain periods.
    - `_date` VALID.
    - `file_name` VALID.
    - `x0-9` INVALID. Cannot contain dashes.
    - `file1` VALID.
    - `Slimit` VALID.

2. **Suppose that your HOME directory is /users/ steve and that you have subdirectories as shown in the following figure:**

    **FIGURE OMITTED**
    
    **Assuming that you just logged in to the system and executed the following commands:**

    - `$ docs=/users/steve/documents`
    - `$ let=$docs/letters`
    - `$ prop=$docs/proposals`
    
    **Write the commands in terms of these variables to**

    - List the contents of the documents directory: `ls $docs`
    - Copy all files from the letters directory to the proposals directory: `cp -R "$let"/* "$prop/"`
    - Move all files whose names contain a capital letter from the letters directory to the current directory. `mv $let/*[A-Z]* .`
    - Count the number of files in the memos directory: `ls "$docs/memos" | wc -l`
       
    **What would be the effect of the following commands?**

    - `ls $let/..` Prints the contents of the documents directory.
    - `cat $prop/sys.A >> $let/no.JSK` Concatenates the contents of `sys.A` to the end of `no.JSK`.
    - `echo $let/*` Prints the file paths of the contents of the `users/steve/documents/letters/` directory.
    - `cp $let/no.JSK $progs`: Error because `$progs` is undefined.
    - `cd $prop` Changes to the `proposals` directory.

3. **Write a program called `nf` to display the number of files in your current directory. Type in the program and test it out.**

    - `touch nf`
    - `chmod +x nf`
    - `echo "ls | wc -l" > nf`
    - `./nf`

4. **Write a program called `whos` to display a sorted list of the logged-in users. Just display the usernames and no other information. Type in the program and test it out.**

    - `touch whos`
    - `chmod +x whos`
    - `echo "users" > whos`

5. **Given the following assignments:**

    - `$ x=*`
    - `$ y=?`
    - `$ z ='one
             two
             three'`
    - `$ now=$(date)`
    - `$ symbol=' >'`
    
    And these files in your current directory:

        $ echo *
        names test1 u vv zebra

    What will the output be from the following commands?
    
    - `echo *** error ***`: names test1 u vv zebra error names test1 u vv zebra
    
    - `echo 'Is 5 * 4 > 18 ?'`: Is 5 * 4 > 18 ?
        
    - `echo $x`: names test1 u vv zebra
    
    - `echo What is your name?`: What is your names
    
    - `echo $y`: u
    
    - `echo Would you like to play a game?`: u echo Would you like to play a game?
    
    - `echo "$y"`: ?
    
    - `echo \*\*\*`: ***
    
    - `echo $z | wc -l`: 1
    
    - `echo \$$symbol`: $>
    
    - `echo "$z" | wc -l`: 3
    
    - `echo $\$symbol`: $$symbol
    
    - `echo '$z' I wc -l`: $z I wc -l
    
    - `echo "\"`: Bash prompt.
    
    - `echo _$now_`: _
    
    - `echo "\\"`: \
    
    - `echo hello $symbol out`: hello > out
    
    - `echo \\`: \
    
    - `echo "\""`: "
    
    - `echo I don't understand`: Bash prompt.
    
6. Write the commands to remove all the space characters stored in the shell variable text. Be sure to assign the result back to text. First use tr to do it and then do the same thing with sed.

    - `text=$(echo $text | tr -d ' ')`
    - `text=$(echo $text | sed 's/ //g')`
    
7. Write the commands to count the number of characters stored in the shell variable text. Then write the commands to count all the alphabetic characters. (Hint: Use sed and wc.) What happens to special character sequences such as \n if they’re stored inside text?:

    - `echo -n $text | wc -c`
    - `echo "012910He8329LLO382  W03ORLD8393" | sed 's/[0-9]//g' | wc -c`
    
8. Write the commands to assign the unique lines in the file names to the shell variable namelist.

    - `namelist=$(sort names | uniq)`
    - `echo "$namelist" | wc -l`
    
