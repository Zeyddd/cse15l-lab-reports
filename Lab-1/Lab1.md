# Remote access

## What you'll be learning

* Installing VScode
* Remotely Connecting
* Trying Some Commands
* Moving Files with scp
* Setting an SSH Key
* Optimizing Remote Running

## 1. Installing VScode

Visit [VSCode_Install](https://code.visualstudio.com/) and download VSCode by following the instructions on the official webpage. You should be greeted with this after a successful download:

![VSCode_ss](/Lab-1/vscode.png)

## 2. Remotely Connecting

You want to begin by installing [OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)

**Make sure you only download the client version!**

Next, go into your VSCode terminal, (either through Ctrl + `, or  Terminal --> New Terminal) and enter the following:

`ssh cs15lfa22kw@ieng6.ucsd.edu`

*Note: The last two letters, after "fa22" is specific to your account, find it through:*

[UCSD accounts](https://sdacs.ucsd.edu/~icc/index.php)

If it's your first time remotely connecting, you're going to be met with the following:

```
⤇ ssh cs15lfa22kw@ieng6.ucsd.edu
The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established. 
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
Are you sure you want to continue connecting (yes/no[fingerprint])?
```
Simply type in `yes` then press enter. You'll be prompted with your password, so type it in, then press enter.

*Note: While entering your password, nothing will show up on the terminal, however, your keystrokes are still being read.*

Congratulations! You've successfully connected to the remote servers!

## 3. Trying some commands

Below is a list of useful commands which I would recommend trying:

* `cd ~`
* `cd`
* `ls -lat`
* `ls -a`
* `ls <directory>` 
* `cat <file>/<directory>`
* `logout`

## 4. Moving files from local to remote

We'll be using a command called `scp`, which we run when copying files from the client (local) machine to the remote one.

Create a file called *test.txt*, and fill it with the following:

`Hello world! I've remote copied this!`

Next, in the terminal, run the following command:

`scp text.txt cs15lfa22kw@ieng6.ucsd.edu:~/`

You'll be prompted for your password, enter it.

Next, log into your remote account using `ssh`, and use `ls`. You'll notice the file test.txt will be there.

Try using `cat test.txt`. What do you notice?

## 5. Setting an SSH key

Here, we'll be creating a special key that will allow us to login much faster.

Start with running this on your local machine:

`ssh-keygen`

You'll be given the following prompt:
```
Enter file in which to save the key (/Users/Zeyad/.ssh/id_rsa):
```
Simply press enter.

Next, enter a short password phrase, that'll make it quicker to login.

Next, log into your ssh account, then enter the following:

`mkdir .ssh`

Then, logout, and enter the following:

```
scp /Users/Zeyad/.ssh/id_rsa.pub cs15lfa22kw@ieng6.ucsd.edu:~/.ssh/authorized_keys
```

Congratulations, you've set up a custom, short passcode for ease of access!

## 6. Optimizing Remote Running

Although we have set up an easier method to enter our password, typing out `ssh cs15lfa22kw@ieng6.ucsd.edu` is still quite time consuming. Therefore, in order to save even more time, here are a few ways of saving some time:

* If its your first time logging in from a fresh terminal, you can always have that line of code copied and saved in a document where you can easily copy paste it

* If it isn't your first time logging in, notice the number when running codes in your terminal: `[cs15lfa22kw@ieng6-203]:~:21$`, the 21 in this case tells us that this will be the twenty first instruction we tell the computer. If you find this number when you first logged in, and then type `! (number)`, it'll run the code you entered for that line, in this case being your login, and save you loads of time!

* When copying files from local to remote, we can once again have our usernamee saved in a document where we can simply paste it instead of fully typing out the entire section