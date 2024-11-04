# **<u>LEVEL0</u>**

Type this command in windows command prompt:

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

Password:

```bash
bandit0
```

# **<u>LEVEL(0-1)</u>**

COMMAND: **ls**

RESULT:**shows readme file**

COMMAND:**cat readme**

RESULT:**shows the password in the file**

PASSWORD:**ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If**

# **<u>LEVEL(1-2)</u>**

COMMAND:**ls**

RESULT:**shows - file**

COMMAND:**cat  ./-**

RESULT:**shows the password in the file**

PASSWORD:**263JGJPfgU6LtdEvgfWU1XP5yac29mFx**

# **<u>LEVEL(2-3)</u>**

COMMAND:**ls**

RESULT:**shows (spaces in this filename) file**

COMMAND:**cat spaces\ in\ this\ filename**

RESULT:**shows the password**

PASSWORD:**MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx**

# **<u>LEVEL(3-4)</u>**

COMMAND:**ls**

RESULT:**shows (inhere) directory**

COMMAND:**cd inhere**

RESULT:**goes to (inhere) directory**

COMMAND:**ls -a**

RESULT:**.    .  .   .  .  .Hiding-From-You**

COMMAND:**cat   . . .Hiding-From-You**

RESULT**:shows the password**

PASSWORD:**2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ**

# **<u>LEVEL(4-5)</u>**

COMMAND:**ls**

RESULT:**shows (inhere) directory**

COMMAND:**cd inhere**

RESULT:**goes to (inhere) directory**

COMMAND:**ls**

RESULT:**shows files from file00 to file09**

COMMAND:**type ./-file00**

RESULT:**Shows the type of the file.If it is ASCII text.Then we got the right password.Check it for every file.**

PASSWORD:**4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw**

# **<u>LEVEL(5-6)</u>**

COMMAND:**ls**

RESULT:**shows (inhere) directory**

COMMAND:**cd inhere**

RESULT:**shows directories from 00 to 19**

COMMAND:**find -readable  -size 1033c !  -executable**

RESULT:**./maybehere07/. file2**

COMMAND:**cd maybehere07**

RESULT:**goes to directory maybehere07**

COMMAND:**cat .file2**

RESULT:**shows  the password**

PASSWORD:**HWasnPhtq9AVKe0dmk45nxy20cvUa6EG**

# **<u>LEVEL(6-7)</u>**

COMMAND:****find / -user bandit7 -group bandit6  -size 33c**

RESULT:**shows all the files only one is given permission other files are permission denied**

EXPLAINATION:**we will copy the file which was given permission  that is /var/lib/dpkg/info/bandit7.password**

COMMAND:**cat  /var/lib/dpkg/info/bandit7.password**

RESULT:**shows the password**

PASSWORD:**morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj**

# **<u>LEVEL(7-8)</u>**

COMMAND:**ls**

RESULT:**shows data.txt file**

COMMAND:**cat data.txt**

RESULT:**shows contents in data.txt file**

COMMAND:**less data.txt**

RESULT:**shows some contents in data.txt file**

COMMAND:**/millionth**

RESULT:**finds out where the word millionth is in file and password is beside it**

PASSWORD:**dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc**

# **<u>LEVEL(8-9)</u>**

COMMAND:**ls**

RESULT:**shows data.txt file**

COMMAND:**cat data.txt**

RESULT:**shows content in data.txt**

COMMAND:**sort data.txt | uniq -u**

EXPLAINATION:**it picks only uniques lines in the file**

RESULT:**shows the password**

PASSWORD:**4CKMh1JI91bUIZZPXDqGanal4xvAg0JM**

# **<u>LEVEL(9-10)</u>**

COMMAND:**ls**

RESULT:**shows data.txt file**

COMMAND:**cat data.txt **

RESULT:**shows contents in data.txt file**

COMMAND:**grep  -o ==== data.txt**

RESULT:**grep  data.txt:binary file matches**

EXPLAINATION:**after sequence of ==== human readable password is present**

PASSWORD:**FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey**

# <u>LEVEL(10-11)</u>

COMMAND:**ls**

RESULT:**Shows data.txt file**

COMMAND:**base64 -d data.txt**

EXPLAINATION:**De encrypts the data.txt file**

RESULT:**Password is obtained**

# <u>LEVEL(11-12)</u>

COMMAND:**ls**

RESULT:**Shows the data.txt file**

COMMAND:**cat data.txt**

RESULT:**Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4**

COMMAND:**echo 'Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4' | tr 'A-Za-z' 'N-ZA-Mn-za-m'**

RESULT:**Shows the password**
