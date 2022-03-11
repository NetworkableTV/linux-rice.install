# Linux rice/install script
This is my all in one linux installer and rice scripts.

## Functions
There is an arch linux installer (originally forked from [ChrisTitus/ArchTitus](https://github.com/ChrisTitusTech/ArchTitus)) and a few scripts for installing custom .dotfiles so ricing is easy (with the desktops preconfigured)

# Arch Linux install script
## Create Arch ISO or Use Image

Download ArchISO from <https://archlinux.org/download/> and put on a USB drive with [Etcher](https://www.balena.io/etcher/), [Ventoy](https://www.ventoy.net/en/index.html), or [Rufus](https://rufus.ie/en/)

## Boot into Arch Linux ISO

From initial Prompt type the following commands:

```
pacman -Sy git
git clone https://github.com/NetworkableTV/linux-rice.install
cd linux-rice.install
./riceinstall.sh
```


### System Description
This is completely automated arch install (your)selected desktop environment on arch using all the packages I use on a daily basis.

## Troubleshooting

__[Arch Linux Installation Guide](https://github.com/rickellis/Arch-Linux-Install-Guide)__

### No Wifi

You can check if the WiFi is blocked by running `rfkill list`.
If it says **Soft blocked: yes**, then run `rfkill unblock wifi`

After unblocking the WiFi, you can connect to it. Go through these 5 steps:

#1: Run `iwctl`

#2: Run `device list`, and find your device name.

#3: Run `station [device name] scan`

#4: Run `station [device name] get-networks`

#5: Find your network, and run `station [device name] connect [network name]`, enter your password and run `exit`. You can test if you have internet connection by running `ping google.com`, and then Press Ctrl and C to stop the ping test.
