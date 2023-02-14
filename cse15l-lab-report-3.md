# Researching Commands: grep command

For all of these examples, my knowledge of these commands was a combination of the information on this [website](https://www.geeksforgeeks.org/grep-command-in-unixlinux/) as well as the information available by using the ```grep --help``` command in the terminal.

## Command Line Option:  ```grep -c <<String>> <<File>> ```
  Example 1:
```
$ grep -c "Fifty" written_2/non-fiction/OUP/Abernathy/*.txt
written_2/non-fiction/OUP/Abernathy/ch1.txt:1
written_2/non-fiction/OUP/Abernathy/ch14.txt:0
written_2/non-fiction/OUP/Abernathy/ch15.txt:0
written_2/non-fiction/OUP/Abernathy/ch2.txt:0
written_2/non-fiction/OUP/Abernathy/ch3.txt:0
written_2/non-fiction/OUP/Abernathy/ch6.txt:0
written_2/non-fiction/OUP/Abernathy/ch7.txt:0
written_2/non-fiction/OUP/Abernathy/ch8.txt:0
written_2/non-fiction/OUP/Abernathy/ch9.txt:0
```
  Example 2:
```
$ grep -c "textile" written_2/non-fiction/OUP/Abernathy/*.txt
written_2/non-fiction/OUP/Abernathy/ch1.txt:24
written_2/non-fiction/OUP/Abernathy/ch14.txt:6
written_2/non-fiction/OUP/Abernathy/ch15.txt:23
written_2/non-fiction/OUP/Abernathy/ch2.txt:26
written_2/non-fiction/OUP/Abernathy/ch3.txt:2
written_2/non-fiction/OUP/Abernathy/ch6.txt:0
written_2/non-fiction/OUP/Abernathy/ch7.txt:1
written_2/non-fiction/OUP/Abernathy/ch8.txt:4
written_2/non-fiction/OUP/Abernathy/ch9.txt:0
```
**What this grep -c command is doing is performing the normal scanning function of grep however instead of printing the lines and lines of text to the terminal, instead there is a simple output of how many times a given string is counted in each file. This, aside from the added benefit of being much cleaner and easier to read than a wall of printed text, also has the benefit of offering the number of times a given string was found, which could be useful in its own way.**
## Command Line Option: ```grep -B n <<String>> <<File>> ```
  Example 1:
```
$ grep -B 2 "Fifty" written_2/non-fiction/OUP/Abernathy/*.txt
written_2/non-fiction/OUP/Abernathy/ch1.txt-
written_2/non-fiction/OUP/Abernathy/ch1.txt-In the late 1940s, Bond Stores, the largest men’s clothing chain at the time, created a sensation in New York City by offering a wide selection of suits with two pairs of pants instead of one, reintroducing a level of product choice not seen since before the war.1 When the line of hopeful buyers at its Times 
Square store stretched around the block, Bond had to impose a limit of two suits per customer. During World War II, the apparel and textile industries had been converted to supply field jackets, overcoats, and uniforms to the U.S. and Allied Forces. But in the years immediately following the war, returning soldiers, the end of rationing, and pent-up customer demand meant apparel was in short supply.
written_2/non-fiction/OUP/Abernathy/ch1.txt:Fifty years later, it is hard to imagine a retailer—be it a high-end department store, mass merchandiser, or catalog service—limiting an individual customer’s clothing purchase. Retailers collect detailed point-of-sales information that reflects the real-time demand for goods by consumers. Through new computer systems, they share this information with suppliers who, in turn, can ship orders within days to automated distribution centers. The contemporary equivalent of Bond Stores now has a much better chance of avoiding stock-outs of popular items and the inventory gluts that lead to costly markdowns. By the same token, the overall risk associated with fickle consumers, numerous selling seasons, and segmented markets—along with fierce overseas competition—has currently made this a tough arena for American retailers and manufacturers.
```
  Example 2:
```
$ grep -B 1 "Dying" written_2/non-fiction/OUP/Abernathy/*.txt
written_2/non-fiction/OUP/Abernathy/ch1.txt-Yet with the signing of the agreements that grew out of the Uruguay Round of international trade negotiations that concluded in 1994, the MFA has now been replaced; textiles and apparel trade are to be integrated into the General Agreement on Tariffs and Trade (GATT) over a ten-year period that ends January 1, 2005. Many American industry participants and policymakers believe these changes could deal a fatal blow to the U.S. apparel industry, which will become even more exposed to global competition. The impact of these trade changes remains uncertain, and national policies that take them into account are still evolving. But if one did not consider the shift in retailing practices that is also recasting the apparel industry—and turned some American companies into unexpected leaders—it might indeed look like “Made in the U.S.A.” was a lost cause.
written_2/non-fiction/OUP/Abernathy/ch1.txt:A Dying Industry—or Not?
```
**What this grep -B n command is doing is finding the line with a given string as normal but in addition to the standard output this command also prints the previous n number of lines, the benefit of this is to add context to the found line.**
  
## Command Line Option: ```grep -n <<String>> <<File>> ```
  Example 1:
```
$ grep -n "Fifty" written_2/non-fiction/OUP/Abernathy/*.txt
written_2/non-fiction/OUP/Abernathy/ch1.txt:6:Fifty years later, it is hard to imagine a retailer—be it a high-end department store, mass merchandiser, or catalog service—limiting an individual customer’s clothing purchase. Retailers collect detailed point-of-sales information that reflects the real-time demand for goods by consumers. Through new computer systems, they share this information with suppliers who, in turn, can ship orders within days to automated distribution centers. The contemporary equivalent of Bond Stores now has a much better chance of avoiding stock-outs of popular items and the inventory gluts that lead to costly markdowns. By the same token, the overall risk associated with fickle consumers, numerous selling seasons, and segmented markets—along with fierce overseas competition—has currently made this a tough arena for American retailers and manufacturers.
```
  Example 2:
```
$ grep -n "Dying" written_2/non-fiction/OUP/Abernathy/*.txt
written_2/non-fiction/OUP/Abernathy/ch1.txt:22:A Dying Industry—or Not?
```
**What this grep -n command is doing is adding the line number of the found line to the front of the terminal and this can be used to find the specific line within the text file itself, no longer reading from the terminal.**
## Command Line Option: ```grep -h <<String>> <<File>> ```
  Example 1:
```
$ grep -h "Fifty" written_2/non-fiction/OUP/Abernathy/*.txt
Fifty years later, it is hard to imagine a retailer—be it a high-end department store, mass merchandiser, or catalog service—limiting an individual customer’s clothing purchase. Retailers collect detailed point-of-sales information that reflects the real-time demand for goods by consumers. Through new computer systems, they share this information with 
suppliers who, in turn, can ship orders within days to automated distribution centers. The contemporary equivalent of Bond Stores now has a much better chance of avoiding stock-outs of popular items and the inventory gluts that lead to costly markdowns. By the same token, the overall risk associated with fickle consumers, numerous selling seasons, and 
segmented markets—along with fierce overseas competition—has currently made this a tough arena for American retailers and manufacturers.
```
  Example 2:
```
$ grep -h "Dying" written_2/non-fiction/OUP/Abernathy/*.txt
A Dying Industry—or Not?
```
**What this grep -h command is doing is removing the directory information from the front of the terminal post and leaving the content of the search, this can make the ```command > file``` functions very useful by excluding the directory information from needlessly being carried into any text proccesses.**
