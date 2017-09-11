# NVIDIA GPU Installation
Instructions for getting your NVIDIA gpu setup and ready to mine on Ubuntu. 

## Locate Driver Version
First, lookup the correct driver to use for you gpu on the [nvidia drivers](https://www.geforce.com/drivers) page. I'm using a GTX 1070 and ended up being pointed to [version 384.69](https://us.download.nvidia.com/XFree86/Linux-x86_64/384.69/NVIDIA-Linux-x86_64-384.69.run).

## Command Line Driver Install 
The easiest way to get the correct driver version onto your system is probably over the command line. You can follow [this guide](http://www.linuxandubuntu.com/home/how-to-install-latest-nvidia-drivers-in-linux) to download the ppa and install the drivers. Substitute the major version number for the version in the guide, so for example replace all instances of 370 with 384. 

Once the setup is complete you should be able to run 
```
nvidia-smi
```

And see the system output all of the nvidia information for your installed drivers and gpu. 

If these steps don't work for you or you'd rather download the exact driver version yourself you can always go the hard way as listed below. 

### Hard Way Driver Install
Install some dependencies before installing the nvidia driver
```
sudo apt-get install linux-headers-amd64 build-essential
```

Then execute 
```
chmod +x NVIDIA-Linux-x86_64-367.35.run
sudo ./NVIDIA-Linux-x86_64-367.35.run
```

At this point the driver installation dialogs will be displayed. You can navigate through these to finish the setup.

If you see this error displayed
```
ERROR: You appear to be running an X server ... 
```
You'll need to run 
```
sudo service lightdm stop
```
And if that doesn't work you can follow the advice listed on [this askubuntu post](https://askubuntu.com/questions/149206/how-to-install-nvidia-run)



