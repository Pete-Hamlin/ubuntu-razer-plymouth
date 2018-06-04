# Ubuntu Razer Logo #

This is an edited Plymouth theme based on the traditional Ubuntu loading splash, however recoloured to use the traditional black/green of Razer, and additionally has a Razer logo added to the centre of the screen above the 'Ubuntu' text (Loading bar also recoloured to Green/White).

I made this initially when I bought my Razer Blade and decided to dual boot with Ubuntu on it. However I've never been a fan of the Ubuntu maroon theme, so figured I'd make my own. Has been tested to work on Ubuntu 16.04 in the Razer Blade 2014.

## Disclaimer ##

This theme was made for my personal use by tweaking a few system configs and adding one custom image. I've decided to release it publicly as the interest in using Linux on Razer systems seems to be on the rise, and if anyone else has the lazy/perfectionist combination I do, I figure they may appreciate this. However, as Plymouth runs during boot, any modifications made to it have the potential to be very dangerous if done wrong, and failing to do things correctly can potentially **break your OS entirely!!**

Therefore, with that being said, you are welcome to use this theme, install it on your PC and make any modifications you like. However, you do this at your own risk, and I will not take any responsibility for corrupted boot sectors, bricked laptops or any other such critical system failures resulting from playing around with system files without due caution. This source code is released entirely without guarantee, and with only 2 bits of advice:
1. Be careful, if all this looks way above your head, probably best to leave this one.
2. May be worth backing up any super critical files, just in case of operator failure.

**You have been warned!!**



## Installation ##

Copy the `ubuntu-logo-razer` folder into your `/usr/share/plymouth/themes/` folder (you will need to use sudo to do this). then run the following in your terminal:

```bash
$ sudo update-alternatives --install /usr/share/plymouth/themes/default.plymouth default.plymouth /usr/share/plymouth/themes/ubuntu-logo-razer/ubuntu-logo-razer.plymouth 100
$ sudo update-alternatives --config default.plymouth
```

From there follow the instructions onscreen, make sure you select the ubuntu-logo-razer theme, then run:
```bash
sudo update-initramfs -u
```

Then enjoy your new theme on boot (feel free to reboot now to check if this has worked).

Also please not this will not get rid of the maroonyness of the GRUB2 menu, please see here for an official tutorial on how to change that:

<https://help.ubuntu.com/community/Grub2/Displays>

## Troubleshooting ##

This theme has been tested as working on Ubuntu 16.04 on the Razer Blade 2014 model. Obviously, I've had no need/means to test it on other platforms, but if you get it working on a different model either with modification or without, you're welcome to submit a pull request or raise an issue and I will update the repo accoringly.

If you're having any problems, feel free to raise an issue and I will do my best to help, but as stated above, I take no responsibility for borked systems (there's probably very little I can do to help you at that point anyway).
