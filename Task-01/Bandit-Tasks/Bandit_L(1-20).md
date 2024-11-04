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

EXPLAINATION:**Decrypts the data.txt file**

RESULT:**dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr**

# <u>LEVEL(11-12)</u>

COMMAND:**ls**

RESULT:**Shows the data.txt file**

COMMAND:**cat data.txt**

RESULT:**Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4**

COMMAND:**echo 'Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4' | tr 'A-Za-z' 'N-ZA-Mn-za-m'**

RESULT:**7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4**

# <u>LEVEL(12-13)</u>

COMMAND:**ls**

OUTPUT:**shows data.txt file**

COMMAND:**mkdir /tmp/bios**

OUTPUT: **a new directory created under /tmp directory**

COMMAND:**cp data.txt /tmp/bios**

OUTPUT:**copies data.txt file into the new directory**

COMMAND:**cd /tmp/bios**

OUTPUT:**shifted to the directory /tmp/bios**

COMMAND:**ls**

OUTPUT:**data.txt**

COMMAND:**xxd -r data.txt > data**

OUTPUT:**decompresses the hexdump file by option -r and normally creates a hexdump file**

COMMAND:**ls**

OUTPUT:**shows the files**

COMMAND:**file data**

OUTPUT:**tells the type of data**

COMMAND:**mv data file.gz**

OUTPUT:**renames the file into .gz format**

COMMAND:**gzip -d file.gz**

OUTPUT:**for decompressing**

COMMAND:**file file**

OUTPUT:**tells the type of the file**

COMMAND:**mv file file.bz2**

OUTPUT:**renames the file**

COMMAND:**bzip2 -d file.bz**

OUTPUT:**compresses the file**

COMMAND:**ls**

COMMAND:**mv file file.tar**

OUTPUT:**renames the file**

COMMAND:**tar xf file.tar**

OUTPUT:**to extract a tar archive**

COMMAND:**ls**

COMMAND:**file data5.bin**

OUTPUT:**tells the type of file**

COMMAND:**rm file.tar**

OUTPUT:**removes the file**

COMMAND:**rm data.txt**

OUTPUT:**removes the file**

COMMAND:**mv data5.bin data.tar**

OUTPUT:**renames the file**

COMMAND:**tar xf data.tar**

OUTPUT:**extract the tar archive file**

COMMAND:**ls**

COMMAND:**file datat6.bin**

OUTPUT:**tells the type of file**

COMMAND:**mv data6.bin data.bz2**

OUTPUT:**renames the file**

COMMAND:**bzip2 -d data.bz2**

COMMAND:**mv data data.tar**

OUTPUT:**renames the file**

COMMAND:**tar xf data.tar**

COMMAND:**file data8.bin**

OUTPUT:**tells the type of the file**

COMMAND:**mv data8.bin data.gz**

OUTPUT:**renames the file**

COMMAND:**gzip -d data.gz**

COMMAND:**file data**

OUTPUT:**tells the type of data file**

COMMAND:**cat data**

OUTPUT:**FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn**

# **<u>LEVEL(13-14)</u>**

COMMAND:**ls** 

OUTPUT:**sshkey.private**

COMMAND(2):**ssh -p 2220 -l bandit14 -i sshkey.private bandit.labs.overthewire.org**

OUTPUT(2):**goes to bandit level14**

# **<u>LEVEL(14-15)</u>**

COMMAND(1):**cat /etc/bandit_pass/bandit14**

OUTPUT(1):**gives the password that is to be submitted to the localhost**

COMMAND:**nc localhost 30000**

OUTPUT:**8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo**

# **<u>LEVEL(15-16)</u>**

COMMAND:**cat /etc/bandit_pass/bandit15**

OUTPUT:**gives the password the previous level's password**

COMMAND:**ncat --ssl localhost 30001**

OUTPUT:**gives the final password**

# **<u>LEVEL(16-17)</u>**

COMMAND:**cat /etc/bandit_pass/bandit16**

OUTPUT:**gives the password that is to be submitted in local host**

COMMAND:**nmap localhost -p 31000-32000**

OUTPUT:**gives the port numbers which have server in them**

PORT STATE SERVICE
31046/tcp open unknown
31518/tcp open unknown
31691/tcp open unknown
31790/tcp open unknown
31960/tcp open unknown

COMMAND:**ncat --ssl localhost 31406**

OUTPUT:**just checking if this the right port.but it is not :(**

COMMAND:**ncat --ssl localhost 31518**

OUTPUT:**just checking if this the right port.but it is not :(**

COMMAND:**ncat --ssl localhost 31691**

OUTPUT:**just checking if this the right port.but it is not :(**

COMMAND:**ncat --ssl localhost 31790**

OUTPUT:**kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx**

# <u>LEVEL(17-18)</u>
