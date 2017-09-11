# NVIDIA GPU Installation
Instructions for getting your NVIDIA gpu setup and ready to mine on Ubuntu. 

## Download Driver
First, lookup the correct driver to use for you gpu on the [nvidia drivers](https://www.geforce.com/drivers) page. I'm using a GTX 1070 and ended up being pointed to [version 384.69](https://us.download.nvidia.com/XFree86/Linux-x86_64/384.69/NVIDIA-Linux-x86_64-384.69.run). You can download this on Ubuntu by navigating to the directory you want to store the file and running a `wget` command
```
wget https://us.download.nvidia.com/XFree86/Linux-x86_64/384.69/NVIDIA-Linux-x86_64-384.69.run
```

## Install Driver
