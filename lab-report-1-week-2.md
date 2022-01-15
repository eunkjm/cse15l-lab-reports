
# **Lab Report 1 : Remote Access**

**Part 1 - Istalling Visual Studio Code**

Go to: [Visual Studio Code Webstite](https://code.visualstudio.com/)

Depending on your computer's operating system, download the appropriate version of the vs code and install it on your computer.

After the installation, open up a new window of VS code. It should look something like this.
(The color of the window might be differnet due to different setting.)

![image]

**Part 2 - Remote Connections**

This part requires a course-specific account.
To find your CSE 15L account, go to [UCSD Account Lookup](https://sdacs.ucsd.edu/~icc/index.php)
and look for an account that starts with cs15ll.

In order to use this account, it needs to be activated by changing the password. (It could take up to 30 minutes for the passworde change to be finalized.)

While waiting for the password changed to be finalized, install OpenSSH using the link below:

[OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)

After installing the OpenSSH, open a new terminal inside of VS Code.
Using the following command line, login to the remote server using the password set during the account activation.
ssh cs15lwi22zz@ieng6.ucsd.edu
(replace zz with your specific id characters)

If you have successfully logged in, the screen wil look like the following:

![image](https://github.com/eunkjm/cse15l-lab-reports/blob/main/vscode.jpg)

**Part 3 - Trying Some Commands**
cd: current directory
ls: list files and directories of the current directory
mkdir: make new directory


**Part 4 - Moving Files with scp**
![image](https://github.com/eunkjm/cse15l-lab-reports/blob/main/scp.jpg)

using the scp command, directory can be copied to the remote server.

**Part 5 - SSH Keys**
![image](https://github.com/eunkjm/cse15l-lab-reports/blob/main/ssh.jpg)

![image](https://github.com/eunkjm/cse15l-lab-reports/blob/main/ssh-keygen.jpg)

**Part 6 - Optimizing Remote Running**





                                                            
                                                
