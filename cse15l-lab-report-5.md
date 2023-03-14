# Researching Commands: grep command

For all of these examples, my knowledge of these commands was a combination of the information on this [website](https://www.geeksforgeeks.org/grep-command-in-unixlinux/) as well as the information available by using the ```grep --help``` command in the terminal.

## Command Line Option:  ```wc -L <<File>> ```
  Example 1:
```
$ wc -L written_2/non-fiction/OUP/Abernathy/*.txt
  1477 written_2/non-fiction/OUP/Abernathy/ch1.txt
  1352 written_2/non-fiction/OUP/Abernathy/ch14.txt
  1506 written_2/non-fiction/OUP/Abernathy/ch15.txt
  1215 written_2/non-fiction/OUP/Abernathy/ch2.txt
  1152 written_2/non-fiction/OUP/Abernathy/ch3.txt
  1743 written_2/non-fiction/OUP/Abernathy/ch6.txt
  1494 written_2/non-fiction/OUP/Abernathy/ch7.txt
  1504 written_2/non-fiction/OUP/Abernathy/ch8.txt
  1229 written_2/non-fiction/OUP/Abernathy/ch9.txt
  1743 total
```
  Example 2:
```
$ wc -L written_2/non-fiction/OUP/Berk/*.txt
  1200 written_2/non-fiction/OUP/Berk/ch1.txt
  1207 written_2/non-fiction/OUP/Berk/ch2.txt
  1310 written_2/non-fiction/OUP/Berk/CH4.txt
  1189 written_2/non-fiction/OUP/Berk/ch7.txt
  1310 total

```
**What this find -L command is doing is returning the width of the text file in characters next to the file name, as opposed to the original count of bytes words and lines that the find command usually outputs. This command could be used in cases such as the grading for our cse12 PAs which have a maximum line width for style points so simply running this command will return an easy answer to whether there are any violations.**
## Command Line Option: ```grep -B n <<String>> <<File>> ```
  Example 1:
```

```
  Example 2:
```

```
**What this grep -B n command is doing is finding the line with a given string as normal but in addition to the standard output this command also prints the previous n number of lines, the benefit of this is to add context to the found line.**
  
## Command Line Option: ```grep -n <<String>> <<File>> ```
  Example 1:
```

```
  Example 2:
```

```
**What this grep -n command is doing is adding the line number of the found line to the front of the terminal and this can be used to find the specific line within the text file itself, no longer reading from the terminal.**
## Command Line Option: ```grep -h <<String>> <<File>> ```
  Example 1:
```

```
  Example 2:
```

```
**What this grep -h command is doing is removing the directory information from the front of the terminal post and leaving the content of the search, this can make the ```command > file``` functions very useful by excluding the directory information from needlessly being carried into any text proccesses.**
