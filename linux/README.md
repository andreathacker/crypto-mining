# Linux Setup

## Install Linux via Windows

### Create Bootable USB Drive
The first step is to create a bootable usb drive that you can use to install a Linux on any drive of your choosing. So far the best tool I've found to do this is [Rufus](https://rufus.akeo.ie/).

An quick tutorial using Rufus can is located on the [tutorials.ubuntu.com](https://tutorials.ubuntu.com/tutorial/tutorial-create-a-usb-stick-on-windows#0) site. Follow through the setup instructions and you should have a usb stick created with an Ubuntu image ready to install on another disk. 

### Install Linux on a Drive
Before you install Linux you'll want to have a drive ready without any files you want to save. Backup anything you care about because the drive will be reformatted and erased. 

Next, reboot your computer and enter the boot menu. On my computer this can be done by pressing `del` at startup, others might find it can be entered through `F8` at startup. Select the usb drive you created with Rufus as the drive you want to boot from. It should display a Ubuntu installation screen once started. 

Select `Install Ubuntu` and run through the prompts, you'll also want to select the `Erase` option while installing to allocate the full disk towards Linux. Finally, select the drive that you want to install Linux to and the installation process will start. 

### Boot the New Linux Drive!
Once you've finished installing Linux on your slected drive you'll be prompted to restart. If you like you can modify your boot order so that your new Linux drive boots up first too. One thing to keep in mind is that the first time you boot up the OS you'll probably want to disconnect as many devices and drives as possible if you have issues. I've often encountered problems trying to boot a new drive because I had a GPU or the bootable USB stick still inserted and Linux hangs. Go ahead and unplug all usb devices and any GPUs if you run into similar issues. You might need to install drivers for these devices once you get up and running with Linu too. 

## Configure Addition Linux Tools 
The following instructions assume that you are using Linux in the terminal mode. After your machine has started enter `ctrl+alt+F1` to enter this mode and disable the GUI. 

## Install SSH 
If you're like me and normally develop from a MacBook or another laptop you may find it's easier to complete the rest of the setup remotely via SSH. You can follow [this](http://www.makeuseof.com/tag/beginners-guide-setting-ssh-linux-testing-setup/) tutorial to finish this but the installation is very straighforward. 

Execute the following command.
```
sudo apt-get install openssh-server
```

Once you have this check for your ip address with 
```
ifconfig
```

You should see something in a format similar to `192.168.1.1`, you'll use this address to connect to your machine remotely. Now you can login from another computer which has ssh installed by using this command. 
```
ssh username@192.168.1.1
```

## Install Tmux
A very useful tool to run all of your mining scripts is [tmux](https://github.com/tmux/tmux). It allows you to use multiple terminal panes as well as manage background tasks from the terminal. 

Installation is simple
```
sudo apt-get install tmux
```
You can follow [these instructions](https://linoxide.com/how-tos/install-tmux-manage-multiple-linux-terminals/) for more info. 
