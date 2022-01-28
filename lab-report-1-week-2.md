[Lab Report 1](https://rinakaura.github.io/cse-15l-lab-reports/lab-report-1-week-2.html)

## Installing VScode

- Click on this link: [Link](https://code.visualstudio.com/)
- Download VSCode onto your computer.
- When installed, you should end up with a screen like this:
![Image](screenshotlab1.png)
---
## Remotely Connecting

- Open a terminal in VSCode by clicking Terminal > New Terminal on the Apple Bar
- Type this command: 
``` 
$ ssh cs15lwi22atu@ieng6.ucsd.edu 
```
  and replace atu with the letters in your account name
- Enter your password when prompted and you should receive the following text:
![Image](remoteconnecting.png)
---
## Trying Some Commands

- Open a terminal in VSCode
- Try some of the following commands
```
$ cd
$ cd ~
$ ls
$ ls -a
$ ls -alt
$ cp /home/linux/ieng6/cs15lwi22/public/hello.txt ~/
$ cat /home/linux/ieng6/cs15lwi22/public/hello.txt
```
- Here's what some of the commands should look like:
![Image](typingcommands.png)
---
## Moving Files with scp

- Type the following:
```
$ scp filename.java cs15lwi22atu@ieng6.ucsd.edu:~/
```
- Enter your password to log in to ieng6
- You should now see your file:
![Image](scpexample.png)
---
## Setting an SSH Key

- Type 
```
$ ssh-keygen
```
  into your terminal. Your result should look close to:
![Image](sshkeygen.png)
- Copy the public key on the id_rsa.pub file from the .ssh directory on your computer
- Try ssh or scp without entering your password. It should work.
---
## Optimizing Remote Running

- Type quotes around your commands to promptly log in and execute commands. For example, try:
```
$ ssh cs15lwi22@ieng6.ucsd.edu "ls"
```
- To reduce keystrokes, click the up arrow to get past commands or use semicolons to run multiple commands at once
![Image](optimizing remote running.png)
- By calling multiple commands on one line I managed to copy and run WhereAmI.java on a remote server in 116 keystrokes, saving me 9 keystrokes.
