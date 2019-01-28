# A Guide for Setting Up Your Raspberry Pi
by TeeJ

## Introduction

You just got a new raspberry pi and do not know how to use it or maybe you just want to learn more. This guide provides an example of how to setup new users, download applications, and install python packages. It is also meant to keep them permenant, so in case your raspberry pi gets wiped you can go back to where you left off. Keep your pi in the clouds!

## Files in Repo:
### notes.txt

I have written down a bunch of useful commands and links to guids in the notes.txt file. Feel free to use them accordingly.

### raspi.init

This is the file that has all the good stuff in it; the brains of the operation. After installing this file you still will not be able to use it. You will first need to enable this file as an executable file. You can do this by using the chmod u+x command. Next you will need to execute the file. Once you execute the file everything will start downloading. And after everything has been downloaded you will still need to enable a few features with raspi-config. Features like vnc, ssh, and the proper screen resolution. Note the difference: Vnc (connecting via a different network) vs ssh (connecting within the same network). For VNC I use VNC Viewer and it seems to work delightfully.

## Steps for Initializing Raspberry Pi
Follow the steps carefully and enjoy:

**1. Open the terminal and go to the desired directory.**

Note: {directory} is a placeholder for the directory you would like to move into.
```shell
ls
cd {directory}
ls
cd ..
ls
```
**2. Clone the repo with github to the current directory.**

Type in the following script to download Git and clone (download) the files to the current directory.
```shell
sudo apt-get install git
sudo git clone "https://www.github.com/teejl/setup_raspi.git"
```
**3. Edit the raspi.init file to your custom settings**

Type in the following command to enter the file and make changes.
```shell
sudo nano raspi.init
```
make changes. then type ctrl + x to exit and y to save.

**4. Enable and Execute raspi.init**

Type in the following commands to enable the raspi.init file to become executable and execute it. It will take a moment to download everything
```shell
sudo chmod u+x raspi.init
sudo ./raspi.init
```

**5. Enable VNC, SSH, and change Screen Resolution.**

Type in the following commands to your terminal.
```shell
sudo raspi-config
```
The Raspberry Pi Software Configuration Tool will come up. Navigate down to "Interfacing Options" and press enter. Enable SSH and VNC. Go back to the Raspberry Pi Software Configuration Tool's home screen and go to "Advanced Options" -> "Resolution" -> {Desired Screen Resolution}.

The Raspberry Pi will reboot, and everything will be configured. Enjoy!
