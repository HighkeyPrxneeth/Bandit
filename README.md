
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

The file is located in a directory named `inhere` which contains a hidden file named `.hidden`. To read the contents of this file, first change the directory.

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

The file is located in a directory named `inhere` which contains a lot of files going by the name `-file0X`. If we `cat` these files, we will get random characters but one of these files contains the password. To find the correct file and read the password, first go into the directory.

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

The password for the next level is stored in the file data.txt and is preceded by several '=' characters. The strings command extracts sequences of printable characters from the binary file, and then grep searches for lines starting with '='.

    strings data.txt | grep -o '==*.*'

<details>
<summary>Password Obtained</summary>

`G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s`
</details>

### [Level 10 -> Level 11](https://overthewire.org/wargames/bandit/bandit11.html)

Connect to the bandit's shell using this command:

    ssh bandit10@bandit.labs.overthewire.org -p 2220

The password for the next level is stored in a file called data.txt, which contains base64 encoded data. You can decode the content of the file using the base64 command and then analyze the output to find the password.

    base64 -d data.txt | cat -

This command decodes the content of data.txt and outputs it in the terminal in ASCII text.
<details>
<summary>Password Obtained</summary>

`6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM`
</details>

### [Level 11 -> Level 12](https://overthewire.org/wargames/bandit/bandit12.html)

Connect to the bandit's shell using this command:

    ssh bandit11@bandit.labs.overthewire.org -p 2220

The password for the next level is stored in a file called data.txt, which contains ROT13 encoded data. You can decode the content of the file using the tr command to perform the ROT13 decoding.

    cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'

This command translates the characters in data.txt using ROT13 encoding.
<details>
<summary>Password Obtained</summary>

`JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv`
</details>

### [Level 12 -> Level 13](https://overthewire.org/wargames/bandit/bandit13.html)

Connect to the bandit's shell using this command:

    ssh bandit12@bandit.labs.overthewire.org -p 2220

The operations that are to be performed are not suitable for home directory. Hence, create a temporary directory in `/tmp` and copy the data.txt file into that directory.

    mkdir /tmp/foxy
    cp data.txt /tmp/foxy/data
    cd /tmp/foxy

If we `cat` this file's header, we should be able to see the data for a file named `data2.bin`. Also check the hex data of the file. It starts with `1f` `8b`, which is the [magic number](https://en.wikipedia.org/wiki/List_of_file_signatures) of gzip compressed files.

    cat data | head

To operate on this file, we have to convert this hex data into an actual file, i.e., revert the data. We can do that using the following command.

    xxd -r data c_data.gz

Now we can decompress the file using this command.

    gzip -d c_data.gz

Now if we check the hex data of the decompressed file, we can see that it starts with `42` `5a` `68` which is also the magic number of bzip2 compressed files. We can rename and decompress this file using the following command.

    mv c_data c_data.bz2
    bzip2 -d c_data.bz2

Again if we check the hex data of the decompressed file, we will find the magic number of gzip compressed files. Rename it and decompress it again.

    mv c_data c_data.gz
    gzip -d c_data.gz

Checking the hex data of the file says almost nothing about it, but if we plainly `cat` the file, we will find strings with the value `ustar` which is the `ISO` encoding for `tar` compressed files. Rename and decompress this file.

    mv c_data c_data.tar
    tar -xf c_data.tar

We can find a new file named `data5.bin` in the directory now. If we `cat` it, we will find `ustar` again. Decompress it.

    tar -xf data5.bin

A new file `data6.bin` appeared now. Looking at it's hex data, we can say that its a bzip2 compressed file. Decompress it.

    bzip2 -d data6.bin

You might get a warning saying that bzip2 couldn't guess the name for the output file. As it is a compressed file, it is normal to see this. Now if we `cat` this file, we will find that `data6.bin.out` is a tar compressed file. Decompress it.

    tar -xf data6.bin.out

Check the hex data of the newly formed file `data8.bin`. You can see that its a gzip compressed file. Rename it and decompress it (for the last time).

    mv data8.bin data8.gz
    gzip -d data8.gz

Now `cat` the `data8` file for the password. The directory and the files that you have created will automatically get deleted (because you made them in `/tmp`, AKA temporary directory).

<details>
<summary>Password Obtained</summary>

`wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw`
</details>

