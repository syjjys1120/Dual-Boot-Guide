# Dual-Boot-Guide
This is about the process and some problems I have gone through during installing dual boot system (Ubuntu 18.04 along with Windows 10) on my Alienware aurora R7 desktop. 

Recently, I want to install Dual Boot system on my desktop to play around with Tensor flow because I heard Linux environment has better support. (Or maybe it's wrong.)

But anyway, I started to install Ubuntu as the second boot system, I thought it probably would take half day of my weekend to get everything set, but turns out I spent the whole week!! Actually 3 whole days (all weekends). I made a stupid decision and that wasted me almost two days.. 

Here is how I installed, failed, google, failed again, google again ...  failed a lot and finally got it work. And a few sincere suggestions I hope would be helpful.

Okay, first here is my PC info:
- Alienware Aroura R7
- Major system: Windows 10
- Second boot: Ubuntu 18.04
- SSD (512G) + HDD (2T)
- Nvidia Geforce GTX 1080 Ti (this might be unrelated)
- Bios boot: UEFI mode. Legacy mode disabled.
- Bios Advanced SATA type: Raid on

1. Make a bootable usb with Ubuntu 18.04

After donwloading Ubuntu 18.04 64 bit.

I followed the video here: https://www.youtube.com/watch?v=qNeJvujdB-0&t=260s
But turns out, it's a little bit different from my request because the video only show's how to make it bootable in legacy mode (MBR). But we need UEFI (GPT) bootable drive.
So I checked out this link https://www.pcsuggest.com/dual-boot-windows-10-and-ubuntu-uefi/ , we need to set partition schema to GPT.

**Suggestion1: Your usb drive will be formatted while using Rufus to build the bootable system, so please backup if necessary.

2. Partition the disk on Windows 10

**Suggestion2: My windows system is installed on SSD, and make sure you also install Ubuntu on the same hard drive (SSD), otherwise there is a chance you cannot see one of the system after you finish all the dual-boot installation. That is to say, in the grub, you probably won't able to see windows system. So partition is necessary here.

Use Windows 10 Disk Manmagement to shrink SSD drive. Also I was following https://www.pcsuggest.com/dual-boot-windows-10-and-ubuntu-uefi/
I have around 320G free space on my SSD (C:/), so I shrink 80G for my Ubuntu 18.04, there are many articles/blog talking about how many space you should shrink, so skipped here. But consider 25G (asked by Ubuntu 18) + 1.5 * memory space + 5G (boot size, home folder and etc) should be enough. So here, I left 80G for Ubuntu.

2.5 Turnoff fast startup
https://www.youtube.com/watch?v=qNeJvujdB-0&t=260s

3. Boot from usb.
Restart your pc, press F2/F12 get into Bios settings.

**It may differ for different machines to get into Bios settings, so maybe not F2/F12 for you.


TBC


