
# Bandit Report

A comprehensive solution-cum-guide to bandit challenges until level 20 and also a report submission for my fellow club-mates.


# Bandit Report

A comprehensive solution-cum-guide to bandit challenges until level 20 and also a report submission for my fellow club-mates.


## Solutions

### [Level 0](https://overthewire.org/wargames/bandit/bandit0.html)

????????? Connect to the bandit's shell using this command.

    ssh bandit0@bandit.labs.overthewire.org -p 2220
<details>
<summary>Password</summary>
    
`bandit0`
</details>

### [Level 0 -> Level 1](https://overthewire.org/wargames/bandit/bandit1.html)

To read the contents in the `readme ` file, use the following command.
    
    cat readme

<details>
<summary>Password Obtained</summary>

`NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL` 
</details>

### [Level 1 -> Level 2](https://overthewire.org/wargames/bandit/bandit2.html)

Connect to the bandit's shell using this command.

    ssh bandit1@bandit.labs.overthewire.org -p 2220

The file named `-` has the password for the next level. To read the contents in that file, use the following command.

    cat ./-

<details>
<summary>Password Obtained</summary>

`rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi` 
</details>

### [Level 2 -> Level 3](https://overthewire.org/wargames/bandit/bandit2.html)

Connect to the bandit's shell using this command.

    ssh bandit2@bandit.labs.overthewire.org -p 2220

The file named `spaces in this filename` has the password for the next level. There are two ways to read the contents in this file.

    cat spaces\ in\ this\ filename

and 

    cat "spaces in this filename"
<details>
<summary>Password Obtained</summary>

`aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG` 
</details>

### [Level 3 -> Level 4](https://overthewire.org/wargames/bandit/bandit2.html)

Connect to the bandit's shell using this command.

    ssh bandit3@bandit.labs.overthewire.org -p 2220

The file is located in a folder named `inhere` which contains a hidden file named `.hidden`. To read the contents of this file, first change the directory.

    cd inhere

And then type `cat` and hit TAB key to get this.

    cat .hidden
<details>
<summary>Password Obtained</summary>

`2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe` 
</details>

### [Level 4 -> Level 5](https://overthewire.org/wargames/bandit/bandit2.html)

Connect to the bandit's shell using this command.

    ssh bandit4@bandit.labs.overthewire.org -p 2220

The file is located in a folder named `inhere` which contains a lot of files going by the name `-file0X`. If we `cat` these files, we will get random characters but one of these files contains the password. To find the correct file and read the password, first go into the folder.

    cd inhere

And then type the following command to get the data type of contents in those files. 

    find ./* 
You will find that `-file07` has `ASCII text` as its data type. Use `cat` to read the contents.

    cat ./-file07
<details>
<summary>Password Obtained</summary>

`lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR` 
</details>


### [Level 5 -> Level 6](https://overthewire.org/wargames/bandit/bandit6.html)

Connect to the bandit's shell using this command.

    ssh bandit5@bandit.labs.overthewire.org -p 2220

The password for the next level is stored in a file within the inhere directory and is human-readable, beginning with '3' and ending with 'd'. You can find it using the find command combined with grep.


    cd inhere
    find . -type f -size 1033c

This command searches for non-executable files in the current directory (inhere) with a size of exactly 1033 bytes.
<details>
<summary>Password Obtained</summary>

`P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU`
</details>

### [Level 6 -> Level 7](https://overthewire.org/wargames/bandit/bandit7.html)

Connect to the bandit's shell using this command.

    ssh bandit6@bandit.labs.overthewire.org -p 2220

The password for the next level is stored in a file somewhere on the server and has the following properties:

    Owned by user bandit7.
    Owned by group bandit6.
    33 bytes in size.

You can find it using the find command combined with file ownership and size specifications.

    find / -user bandit7 -group bandit6 -size 33c 2>/dev/null

<details>
<summary>Password Obtained</summary>

`z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S`
</details>

### [Level 7 -> Level 8](https://overthewire.org/wargames/bandit/bandit8.html)

Connect to the bandit's shell using this command.

    ssh bandit7@bandit.labs.overthewire.org -p 2220

The password for the next level is stored in the data.txt file next to the word "millionth".

You can use grep to search for the word "millionth" in the data.txt file.

    grep millionth data.txt

<details>
<summary>Password Obtained</summary>

`TESKZC0XvTetK0S9xNwm25STk5iWrBvP`
</details>

### [Level 8 -> Level 9](https://overthewire.org/wargames/bandit/bandit9.html)

Connect to the bandit's shell using this command.

    ssh bandit8@bandit.labs.overthewire.org -p 2220

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once.

You can use sort and uniq commands to find the unique line.

    sort data.txt | uniq -u

<details>
<summary>Password Obtained</summary>

`EN632PlfYiZbn3PhVK3XOGSlNInNE00t`
</details>

### [Level 9 -> Level 10](https://overthewire.org/wargames/bandit/bandit10.html)

Connect to the bandit's shell using this command.

    ssh bandit9@bandit.labs.overthewire.org -p 2220

The password for the next level is stored in the file data.txt and is preceded by several '=' characters.

You can use grep to search for lines starting with '='.

    strings data.txt | grep -o '==*.*'

<details>
<summary>Password Obtained</summary>

`G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s`
</details>

