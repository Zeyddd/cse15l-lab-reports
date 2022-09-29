# Remote access

# What you'll be learning

* Installing VScode
* Remotely Connecting
* Trying Some Commands
* Moving Files with scp
* Setting an SSH Key
* Optimizing Remote Running

# 1. Installing VScode

Visit [VSCode_Install](https://code.visualstudio.com/) and download VSCode by following the instructions on the official webpage. You should be greeted with this after successfuly downloading:

![VSCode_ss](/Lab%201/vscode%20ss.png)

# 2. Remotely Connecting

You want to begin by installing [OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)

**Make sure you only download the client version!**

Next, go into your VSCode terminal, (either through Ctrl + `, or  Terminal --> New Terminal) and enter the following:

`ssh cs15lfa22kw@ieng6.ucsd.edu`

*Note*: The last two letters, after "*fa22*" is specific to your account, find it through:

[UCSD accounts](https://sdacs.ucsd.edu/~icc/index.php)

If it's your first time remotely connecting, you're going to be met with the following:

```
⤇ ssh cs15lfa22kw@ieng6.ucsd.edu
The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established. 
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
Are you sure you want to continue connecting (yes/no[fingerprint])?
```
