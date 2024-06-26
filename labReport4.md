## Log in to ieng6
### **ssh `<space>` j7shim@ieng6.ucsd.edu `<enter>`**
![Screenshot](ieng6LogIn.png)
Logged in to the ieng6 server with private key I have on my MacBook. 

***

## Clone My Fork of the Repository from My Github Account (Using the SSH URL)
### **git `<space>` clo `<tab>` `<space>` `<ctrl + v>` `<enter>`**
![Screenshot](cloningFork.png)
Cloned the forked repository from my github account into the ieng6 server. 
* `<tab>`: *automatically fills out the remaining command line. In this case automatically completed 'clone'*
* `<ctrl + v>`: *pastes the ssh url of the forked repository from my github, which was 'git@github.com:jh0726/lab7.git'.*

***

## Run the Tests, Demonstrating That They Fail
### **cd `<space>` l `<tab>` `<enter>`**
### **ls `<enter>`**
### **bash `<space>` te `<tab>` `<enter>`**
![Screenshot](lab4FailedTest.png)
Changed the current directory to lab7 and runned the command lines in test.sh file. 
* `<tab>`: *automatically fills out the remaining command line. In this case automatically completed 'clone'*

***

## Edit the Code File to Fix the Failing Test 
### **vim `<space>` ListExamples.java `<enter>`**
![Screenshot](vim.png)
Used vim to access the code of the java file that produced error and fix it. In this case, the error message indicated the error came from ListExamples.java file. Therefore, tried to access the java code of ListExamples.java file using vim. 

### **:44 `<enter>`**
![Screenshot](line44.png)
Referencing the error message, it indicated that the error came from line 44. To directly move on to line 44 rather than pressing down arrow key 44 times, used ':(line number)' vim command. 

### **5l**
![Screenshot](Right5Times.png)
The error on the line 44 was incorrect index number. Since the incorrect integer was written on the 5th index right from the first index, used 'l(move right)' vim command with the value of number of times moving to right in front of it. 

### **dw**
![Screenshot](delete.png)
To delete the incorrect integer, used 'dw' vim command. As a result, incorrect integer 1 was deleted.

### **i**
![Screenshot](insertMode.png)
In order to add correct integer after the 'index', changed to insertion mode by typing i. 

### **2 `<esc>`**
![Screenshot](fixAndEscape.png)
Added 2 after the index to fix the error (changing index1 to index2). Pressed escape key to change it back to the default mode from the insertion mode. 
* `<esc>`: escape from the current mode and goes back to the default. 

### **:wq `<enter>`**
In order to save the edits I made in the ListExamples,java and exit, used ':wq' vim command. `:wq` represents save and exit. 

***

## Run the Tests, Demonstrating that They Now Succeed
### `<up>` `<up>` `<enter>`
![Screenshot](lab4SuccessTest.png)
Used up arrow key two times to reuse the command line I used in 2 previous command line, which was `bash test.sh`. 
* `<up>`: up arrow key allows to access the command line I used in previous steps rather than typing the entire command. The number of time I use the up arrow, the more previous command line I can access to. 

*** 

## Commit and Push the Resulting Change to My Github Account (Any Commit Message!)
### git `<space>` ad `<tab>` `<enter>`
### git `<space>` com `<tab>` `<space>` -m `<space>` "Error Fixed" `<space>`
![Screenshot](gitPushCommit.png)
'git add .' command adds entire change in the working directory to the staging area. The updates in staging area are being sent and updated at my git repository through the 'git commit' command. In order to successfully commit, I had to include a message after '-m'. The message I chose was 'Error Fixed' to indicate that the error that caused the file to not compile correctly was fixed. 
* `<tab>`: *automatically fills out the remaining command line. In this case automatically completed 'clone'*
