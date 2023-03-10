# Speed Challenge

## Step 4
First thing you need to do is log into your iegn6 account, I did this by typing ```cs15lwi23awj@ieng6.ucsd.edu```, if you have created a ssh key already then that will be all that is needed, otherwise you will need to put in your password as well.

![Image](Step4.JPG)


## Step 5
Then I cloned the directory onto the account by first copying the ssh version of the url from the forked repository on github and then typing ```git clone <ctrl>c``` to input this to the terminal: 

![Image](Step5.JPG)

## Step 6
Here, although unnecessary, I used ```ls <enter>``` to confirm that the directory lab7 had been cloned, then I used ```cd lab7 <enter>``` to change my directory before copy pasting the javac and java commands for junit testing, inputting: ```<ctrl>c <enter>``` then ```<ctrl>c L<tab>Tests <enter>``` to run the tests.

![Image](Step6.JPG)

## Step 7
Then, seeing that there is an error in the code somewhere, I open the ListExamples file by typing ```nano L<tab>.java <enter>``` to open up a text editor in the terminal.

![Image](Step7.1.JPG)

From there I press ```<down>``` and ```<right>``` until I get down to the error in the code and fix it by pressing ```<backspace> 2``` to repace the 1 in input1 with 2, making it input2.

![Image](Step7.2.JPG)

Once these changes have been done I pressed ```<ctrl>o <enter> <ctrl>x``` to save the changes and exit the text editor.

## Step 8
After saving the changes I needed to recompile the java files and rerun the tests, these commands were already in my command history so I reached them by typing ```<up><up><up><enter>``` to compile and ```<up><up><up><enter>``` again to run the tests.

![Image](Step8.JPG)

## Step 9
Now that the tests can run without failures we want to commit these changes to the github version of this code. This is done by typing ```git add L<tab>.java <enter>``` and then ```git commit -m "Corrected Version" <enter>``` and finally ```git push <enter>```

![Image](Step9.JPG)
