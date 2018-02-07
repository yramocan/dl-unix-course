With the session 2 directory as your working directory, start vi.

1. Examine the file `tamarian.txt`. What did you enter to open this file?

    * `:edit tamarian.txt`

2. Go to the eleventh line by entering `11G`. What is the first word
   on this line?
   
    * "Darmok", to be more specific: "Darmok on the ocean".

3. Press `2fo` to move forward to the second "o" on the line. Press
   `2j` to go down two lines. What is the word the cursor is on, as
   well as the one after it?
   
    * "problem to"

4. Press `2w` followed by `k` to move forward two words and then up
   one line. What is the word the cursor is on, as
   well as the one after it?
   
    * "friendship and"

5. Press `7j` to move down 7 lines. What line number are you on now?

    * Line 20

6. Press `/Shaka` followed by Enter to search for the next occurrence
   of "Shaka". What line are you on now?
   
    * Line 22

7. Press `n` to jump to the next occurrence of "Shaka". What line and
   column number are you at now?
   
    * Line 34, Column 66

8. Press `?Jiri` to search backwards for "Jiri". What line and column
   number are you at now?
   
    * Line 27, Column 65

9. Press `7B` to go back 4 (7?) words, ignoring punctuation. Press `cw` to
   change the word. Type "Nathan" and press ESC to exit insert
   mode. What does the sentence say now?
   
    * "Nathan of Lowani" OR "Nathan under two moons"

10. Press `fJ` to move forward to the next instance of "J", Press `ce`
    to change to the end of the word. Type "Dan" and press ESC to exit
    insert mode. What does the sentence say now?
    
    * "Dan of Ubaya"

11. Press `16G` followed by `2fZ` to move to the second occurrence of
    "Z". Press `da"` to cut the text near the cursor between the
    quotation marks, inclusive. What text did you just cut?
    
    * "Zima and Bakor"

12. Press `o` to open a line below the current line and the press
    `ESC` followed by `p` to paste the text cut from the previous
    line. Press `A` to append to the end of the line and add the text
    " - a terrible cocktail from the 90s". What does this line now read?
    
    * `"Zima and Bakor" - a terrible cocktail from the 90s`

13. Press `ESC` to return to normal mode and then `yy` to yank the
    line. Press `P` to paste a copy of this line above the current
    line. What is the line number for the new line you just pasted?
    
    * Line 17

14. Press `:s/Bakor/Jolly Rancher/` to do a search-and-replace. What
    does this line now say?
    
    * `"Zima and Jolly Rancher" - a terrible cocktail from the 90s`

15. Press `j` then `dd` to delete the previous copy of the line. What
    word is your cursor on now?
    
    * "Kiteo"
