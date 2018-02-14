1. **What will be matched by the following regular expressions? (Assume POSIX locale.)**

    - `x*`: All occurrences of the character 'x' at the beginning of a string.
    - `[0-9]\{3\}: A single digit followed by open curly brace, 3, close curly brace.
    - `xx*`: The first occurrence of x and any immediately subsequent x's in a string.
    - `[0-9]\{3,5\}`: A single digit followed by open curly brace, 3, comma, 5, close curly brace.
    - `x\{1,5\}`: The character "x" followed by open curly brace, 3, comma, 5, close curly brace.
    - `[0-9]\{1,3\},[0-9]\{3\}`: A single digit followed by open curly brace, 1, comma, 3, close curly brace, comma, single digit, open curly brace, 3, close curly brace.
    - `x\{5,\}`: The character "x" followed by open curly brace, 5, comma, close curly brace.
    - `^\...`: Dot at beginning of string followed by exactly two non-line-break characters.
    - `x\{10\}`: The character "x" followed by open curly brace, 1, 0, close curly brace.
    - `[A-Za-z_][A-Za-z_0-9]*`: Any string beginning with a letter or underscore, followed by any number of alphanumeric characters.
    - `[0-9]`: The first occurrence of any single digit.
    - `\([A-Za-z0-9]\{1,\}\)\1`: (, any alphanumeric character, {1}, comma, }), start of header character.
    - `[0-9]*`: A number of any length.
    - `^Begin$`: The word "Begin".
    - `[0-9][0-9][0-9]`: Three consecutive single digits.
    - `^\(.\).*\1$`: String that begins with open parenth, any non-line-break char, close parenth, 0 or more non-line-break chars, SOH char, end of string.

2. **What will be the effect of the following commands?**

    - `who | grep 'mary'`
    - `who | grep '^mary'`
    - `grep '[Uu]nix' ch?/*`
    - `ls -l | sort -k 5nr`
    - `sed '/^$/d' text > text.out`
    - `sed 's/\([Uu]nix\)/\1(TM)/g' text > text.out`
    - `date | cut -c12-16`
    - `date | cut -c5-11,25- | sed 's/\([0-9]\{1,2\}\)/\1,/'`

3. **Write commands to:**
    
    a. Find all logged-in users with usernames of at least four characters.
    b. Find all users on your system who's user ids are greater than 99.
    c. Find the number of users on your system who's user ids are greater than 99.
    d. List all the files in your current directory in decreasing order of file size (without using the “-S” option to ls).
