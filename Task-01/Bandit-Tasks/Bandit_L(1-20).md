# **<u>LEVEL0</u>**

Type this command in windows command prompt:

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

Password:

```bash
bandit0
```

# **<u>LEVEL1</u>**

COMMAND(1): **ls**

RESULT(1):**shows readme file**

COMMAND(2):**cat readme**

RESULT(2):**shows the password in the file**

PASSWORD:**ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If**

# **<u>LEVEL2</u>**

COMMAND(1):**ls**

RESULT(1):**shows - file**

COMMAND(2):**cat  ./-**

RESULT(2):**shows the password in the file**

PASSWORD:**263JGJPfgU6LtdEvgfWU1XP5yac29mFx**

# **<u>LEVEL3</u>**

COMMAND(1):**ls**

RESULT(1):**shows (spaces in this filename) file**

COMMAND(2):**cat spaces\ in\ this\ filename**

RESULT(2):**shows the password**

PASSWORD:**MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx**

# **<u>LEVEL4</u>**

COMMAND(1):**ls**

RESULT(1):**shows (inhere) directory**

COMMAND(2):**cd inhere**

RESULT(2):**goes to (inhere) directory**

COMMAND(3):**ls -a**

RESULT(3):**.    .  .   .  .  .Hiding-From-You**

COMMAND(4):**cat   . . .Hiding-From-You**

RESULT(4)**:shows the password**

PASSWORD:**2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ**

# **<u>LEVEL5</u>**

COMMAND(1):**ls**

RESULT(1):**shows (inhere) directory**

COMMAND(2):**cd inhere**

RESULT(2):**goes to (inhere) directory**

COMMAND(3):**ls**

RESULT(3):**shows files from file00 to file09**

COMMAND(4):**cat ./-file00  ./-file01  ./-file02  ./-file03  ./-file04  ./-file05  ./-file06  ./-    file07  ./-file08  ./-file09**

RESULT(4):**shows only 1 humanreadable password**

PASSWORD:**4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw**

# **<u>LEVEL6</u>**

COMMAND(1):**ls**

RESULT(1):**shows (inhere) directory**

COMMAND(2):**cd inhere**

RESULT(2):**shows directories from 00 to 19**

COMMAND(3):**find -readble  -size 1033cc !  -executable**

RESULT(3):**./maybehere07/. file2**

COMMAND(4):**cd maybehere07**

RESULT(4):**goes to directory maybehere07**

COMMAND(5):**cat .file2**

RESULT(5):**shows  the password**

PASSWORD:**HWasnPhtq9AVKe0dmk45nxy20cvUa6EG**

# **<u>LEVEL7</u>**

COMMAND(1):****find / -user bandit7 -group bandit6  -size 33c**

RESULT(1):**shows all the files only one is given permission other files are permission denied**

EXPLAINATION:**we will copy the file which was given permission  that is /var/lib/dpkg/info/bandit7.password**

COMMAND(2):**cat  /var/lib/dpkg/info/bandit7.password**

RESULT(2):**shows the password**

PASSWORD:**morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj**

# **<u>LEVEL8</u>**

COMMAND(1):**ls**

RESULT(1):**shows data.txt file**

COMMAND(2):**cat data.txt**

RESULT(2):**shows contents in data.txt file**

COMMAND(3):**less data.txt**

RESULT(3):**shows some contents in data.txt file**

COMMAND(4):**/millionth**

RESULT(4):**finds out where the word millionth is in file and password is beside it**

PASSWORD:**dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc**

# **<u>LEVEL9</u>**

COMMAND(1):**ls**

RESULT(1):**shows data.txt file**

COMMAND(2)**cat data.txt**

RESULT(2):**shows content in data.txt**

COMMAND(3):**sort data.txt | uniq -u**

EXPLAINATION:**it picks only uniques lines in the file**

RESULT(3):**shows the password**

PASSWORD:**4CKMh1JI91bUIZZPXDqGanal4xvAg0JM**

# **<u>LEVEL10</u>**

COMMAND(1):**ls**

RESULT(1):**shows data.txt file**

COMMAND(2):**cat data.txt **

RESULT(2):**shows contents in data.txt file**

COMMAND(3):**grep  -o ==== data.txt**

RESULT(3):**grep: data.txt:binary file matches**

EXPLAINATION:**after sequence of ==== human readable password is present**

PASSWORD:**FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey**
