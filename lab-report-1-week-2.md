

# **Week 2 Lab Report**
*By: Adhithi Ganesan*

## Step 1: Installing VS Code

[Link to download Visual Studio Code](https://code.visualstudio.com/Download)

Click on the link above to download Visual Studio Code. You should see a page like this:
![Image](vscode)

Click on the download button under the system you are using and it should begin downloading. Continue with the rest of the instructions the VS code prompts you to follow.

---

## Step 2: Remotely Connecting

Use this [Link](https://sdacs.ucsd.edu/~icc/index.php) to find your student account for the CSE 15L course. Then open Visual Studio Code and on the command line, enter:

```
$ ssh cs15lsp22zz@ieng6.ucsd.edu
```

** But replace the zz with the letters in your account. 

Respond yes to the messages when prompted and enter the password to your UCSD account. 

Your terminal should display a message like this once you complete all the steps:

![Image](vscode1)


---

## Step 3: Trying Some Commands

On the terminal, try running some commands like: 
`cd`,
` ls`,
` pwd`, 
`mkdir`, and `cp`. You can try this both on your computer and the remote computer after using `ssh`. If you were to run the command `ls-lat`, you should get an output on the terminal that looks similar to this: 

![Image](vscode2)

---

## Step 4: Moving Files With scp

Create a file called "Slay.java" (it is imperative that you name the file this) and put the following into the file:
```
class Slay {
  public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}
```
Run the file using javac and java and then enter this in the command line of the terminal: 
```
scp slay.java cs15lsp22zz@ieng6.ucsd.edu:~/
```

Log into your ieng6 account again with `ssh` and use `ls`. Your file should now be in the home directory. 

Your output should look something like this:

![Image](vscode3)

----

## Step 5: Setting an `SSH` Key

Run the following code: 
```
# on client (your computer)
$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/<user-name>/.ssh/id_rsa): /Users/<user-name>/.ssh/id_rsa
Enter passphrase (empty for no passphrase): 
```
**DO NOT ENTER A PASSPHRASE!**

This created two files in the .ssh directory in your computer. 

Run the following code next:

```
$ ssh cs15lsp22zz@ieng6.ucsd.edu
<Enter Password>
# now on server
$ mkdir .ssh
$ <logout>
# back on client
$ scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys
# You use your username and the path you saw in the command above
```

Now you won't have to enter your password every time! 

You should get something that looks like this:

![Image](vscode4)

---

## Step 6: Optimizing Remote Running

There are a lot of shortcuts to make remote running easier! 
Some include: 
- Including commands in quotes after entering your ieng6 account. Ex: 
```
$ ssh cs15lsp22zz@ieng6.ucsd.edu "ls"
```
- You can also use semi colons to run multiple commands in one line. Ex:
```
 $ cp WhereAmI.java OtherMain.java; javac OtherMain.java; java Slay
 ```
- You can use the up arrow to copy previous terminal commands and rerun them. 

The last shortcut is my favorite. Especially when I have multiple errors in my code and it won't compile, I can easily change the code and run it using the up arrow instead of using the javac and java commands every time. 

![Image](vscode5)








