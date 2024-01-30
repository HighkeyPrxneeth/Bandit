
# Bandit Report

A comprehensive solution-cum-guide to bandit challenges until level 20 and also a report submission for my fellow club-mates.


## Solutions

### [Level 0](https://overthewire.org/wargames/bandit/bandit0.html)

????????? Connect to the bandit's shell using this command.

    ssh bandit0@bandit.labs.overthewire.org -p 2220
<details>
<summary>Password</summary>
bandit0
</details>

### [Level 0 -> Level 1](https://overthewire.org/wargames/bandit/bandit1.html)

To read the contents in the `readme ` file, use the following command.
    
    cat readme

<details>
<summary>Password</summary>

`bandit0` 
</details>

### [Level 1 -> Level 2](https://overthewire.org/wargames/bandit/bandit2.html)

Connect to the bandit's shell using this command.

    ssh bandit1@bandit.labs.overthewire.org -p 2220

The file named `-` has the password for the next level. To read the contents in that file, use the following command.

    cat ./-

<details>
<summary>Password</summary>

`NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL` 
</details>

### [Level 2 -> Level 3](https://overthewire.org/wargames/bandit/bandit2.html)

Connect to the bandit's shell using this command.

    ssh bandit2@bandit.labs.overthewire.org -p 2220

The file named `spaces in this filename` has the password for the next level. There are two ways to read the contents in this file.

    cat spaces\ in\ this\ filename

and 

    cat "spaces in this filename"
<details>
<summary>Password</summary>

`rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi` 
</details>

### [Level 3 -> Level 4](https://overthewire.org/wargames/bandit/bandit2.html)

Connect to the bandit's shell using this command.

    ssh bandit3@bandit.labs.overthewire.org -p 2220

The file is located in a folder named `inhere` which contains a hidden file named `.hidden`. To read the contents of this file, first change the directory.

    cd inhere

And then type `cat` and hit TAB key to get this.

    cat .hidden
<details>
<summary>Password</summary>

`aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG` 
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
<summary>Password</summary>

`2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe` 
</details>

