# Researching Commands: wc command

For all of these examples, my knowledge of these commands was sourced from the information available by using the ```wc --help``` command in the terminal.

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
**What this wc -L command is doing is returning the width of the text file in characters next to the file name, as opposed to the original count of bytes words and lines that the wc command usually outputs. This command could be used in cases such as the grading for our cse12 PAs which have a maximum line width for style points so simply running this command will return an easy answer to whether there are any violations.**
## Command Line Option: ```wc -m <<File>> ```
  Example 1:
```
$ wc -m written_2/non-fiction/OUP/Abernathy/*.txt
 46547 written_2/non-fiction/OUP/Abernathy/ch1.txt
 39755 written_2/non-fiction/OUP/Abernathy/ch14.txt
 43720 written_2/non-fiction/OUP/Abernathy/ch15.txt
 44505 written_2/non-fiction/OUP/Abernathy/ch2.txt
 34877 written_2/non-fiction/OUP/Abernathy/ch3.txt
 41963 written_2/non-fiction/OUP/Abernathy/ch6.txt
 42182 written_2/non-fiction/OUP/Abernathy/ch7.txt
 52277 written_2/non-fiction/OUP/Abernathy/ch8.txt
 31187 written_2/non-fiction/OUP/Abernathy/ch9.txt
377013 total
```
  Example 2:
```
$ wc -m written_2/non-fiction/OUP/Berk/*.txt
 91069 written_2/non-fiction/OUP/Berk/ch1.txt
101137 written_2/non-fiction/OUP/Berk/ch2.txt
101875 written_2/non-fiction/OUP/Berk/CH4.txt
 65865 written_2/non-fiction/OUP/Berk/ch7.txt
359946 total
```
**What this wc -m command is doing is finding the character count of each file and palcing that number nexxt to the file name, as opposed to the standard output with the count of lines words and bytes. This is useful for finding some approximation of the size of the content within as opposed to the internal dimensions.**
  
## Command Line Option: ```wc -w <<File>> ```
  Example 1:
```
$ wc -w written_2/non-fiction/OUP/Abernathy/*.txt
  6978 written_2/non-fiction/OUP/Abernathy/ch1.txt
  5918 written_2/non-fiction/OUP/Abernathy/ch14.txt
  6544 written_2/non-fiction/OUP/Abernathy/ch15.txt
  6708 written_2/non-fiction/OUP/Abernathy/ch2.txt
  5273 written_2/non-fiction/OUP/Abernathy/ch3.txt
  6689 written_2/non-fiction/OUP/Abernathy/ch6.txt
  6718 written_2/non-fiction/OUP/Abernathy/ch7.txt
  8619 written_2/non-fiction/OUP/Abernathy/ch8.txt
  5331 written_2/non-fiction/OUP/Abernathy/ch9.txt
 58778 total
```
  Example 2:
```
$ wc -w written_2/non-fiction/OUP/Berk/*.txt
 13726 written_2/non-fiction/OUP/Berk/ch1.txt
 15525 written_2/non-fiction/OUP/Berk/ch2.txt
 15677 written_2/non-fiction/OUP/Berk/CH4.txt
 10158 written_2/non-fiction/OUP/Berk/ch7.txt
 55086 total
```
**What this grep -n command is doing is adding the line number of the found line to the front of the terminal and this can be used to find the specific line within the text file itself, no longer reading from the terminal.**
## Command Line Option: ```wc -l <<File>> ```
  Example 1:
```
$ wc -l written_2/non-fiction/OUP/Abernathy/*.txt
    81 written_2/non-fiction/OUP/Abernathy/ch1.txt
    78 written_2/non-fiction/OUP/Abernathy/ch14.txt
    78 written_2/non-fiction/OUP/Abernathy/ch15.txt
    77 written_2/non-fiction/OUP/Abernathy/ch2.txt
    68 written_2/non-fiction/OUP/Abernathy/ch3.txt
    83 written_2/non-fiction/OUP/Abernathy/ch6.txt
    70 written_2/non-fiction/OUP/Abernathy/ch7.txt
    80 written_2/non-fiction/OUP/Abernathy/ch8.txt
    54 written_2/non-fiction/OUP/Abernathy/ch9.txt
   669 total
```
  Example 2:
```
$ wc -l written_2/non-fiction/OUP/Berk/*.txt
   221 written_2/non-fiction/OUP/Berk/ch1.txt
   248 written_2/non-fiction/OUP/Berk/ch2.txt
   313 written_2/non-fiction/OUP/Berk/CH4.txt
   204 written_2/non-fiction/OUP/Berk/ch7.txt
   986 total

```
**What this grep -h command is doing is removing the directory information from the front of the terminal post and leaving the content of the search, this can make the ```command > file``` functions very useful by excluding the directory information from needlessly being carried into any text proccesses.**
