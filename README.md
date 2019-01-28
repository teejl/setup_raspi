# A guide for setting up your Raspberry Pi
by TeeJ

## Introduction

You just got a new raspberry pi and do not know how to use it or maybe you just want to learn more. This guide provides an example of how to setup new users, download applications, and install python packages. It is also meant to keep them permenant, so in case your raspberry pi gets wiped you can go back to where you left off. Keep your pi in the clouds!

## Notes.txt

I have written down a bunch of useful commands and links to guids in the notes.txt file. Feel free to use them accordingly.

## Raspi.init

This is the file that has all the good stuff in it; the brains of the operation. After installing this file you still will not be able to use it. You will first need to enable this file as an executable file. You can do this by using the chmod u+x command. Next you will need to execute the file. Once you execute the file everything will start downloading. And after everything has been downloaded you will still need to enable a few features with raspi-config. Features like vnc, ssh, and the proper screen resolution. Note the difference: Vnc (connecting via a different network) vs ssh (connecting within the same network). For VNC I use VNC Viewer and it seems to work delightfully.

## Procedure for Initializing Raspberry Pi
Follow the steps carefully and enjoy:
1. Clone the repo with github to the current directory (change directory with cd {folder}, cd .. [use to go back], and ls)
```shell
sudo apt-get git
sudo git clone "https://www.github.com/teejl/setup_raspi.git"
```
2. 
