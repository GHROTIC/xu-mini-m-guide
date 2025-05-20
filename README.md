<div align="center">

###### DISCLAIMER: I try to verify information but I'm not perfect and things change daily.<br>Please let me know @GHROTIC in the MagicX Discord if you notice any errors. Guide last updated on May 19th, 2025.

  
  # **-== Xu Mini M Guide==-**

</div>

<br>
  
### ~ Quick Comparison Table of Firmware Features: ~

</div>

| - | Stock | PlumOS | Rocknix | MinUI(MOSS) |
| -- | -- | -- | -- | -- |
| Scraper*(n0): | Yes/No*(n1) | No(Broken) | Yes | No |
| Game Switcher: | No | No | No | No |
| Boot to Game: | No | No | Partial*(n2) | No |
| Wifi Dongle Support | ? | Yes | Yes | No |
| Portmaster: | No | Yes*(n3) | Yes | Yes*(n3) |
| Dreamcast: | ? | Fair | Poor | N/A |
| N64: | ? | Fair | Fair | Fair*(n4) |
| PSP: | ? | Fair | Good*(n5) | N/A |
| PSX: | ? | Good | Good | Good |


###### (Ratings Scale based on: Poor->Fair->Good->Very Good->Excellent)
- n0: Scraper Requires compatible Wifi or Ethernet USB Dongle. Dongle compatability varries based on OS. 
- n1: Scraper is working on Stock Firmware V1 but broken on Stock Firmware V2.
- n2: Rocknix has the option to immediately open a game and continue at the last auto save state when opening a rom file (Retroarch Only).
- n3: Some Portmaster Games will not work due to outdated libraries. Requires the additional Pak below(n4) to support Portmaster on MinUI. 
- n4: Requires Ry Pak: https://github.com/ryanmsartor/XU-Mini-M-Custom-MinUI-Paks
- n5: Rocknix has better performance than PlumOS but some minor audio skipping observed during testing.

<br>

### ~ Performance Testing: ~

[Dreamcast (PlumOS)](https://docs.google.com/spreadsheets/d/e/2PACX-1vRA0rB9W96J_3Y57vl9kGSeiQTYB80dM1LOwPrW2wcXC-7lUwLjK_vUXydUDOUlAGYJ62GQWxg4eDBd/pubhtml)
<br>
[PSP (PlumOS)](https://docs.google.com/spreadsheets/d/e/2PACX-1vSX9Mcinj3PZe8gIyBt-HLdAdc9uOxxbGVLINe2Gi-GULrorNbumlYResiqtvsrhnVNXzdTksaPQGvU/pubhtml)


<br>

## Notes for each OS:

### ~ Stock ~

Modified version of the AmberELEC Firmware that removes many functions and settings. PlumOS almost immediately replaced this Stock Firmware and little testing has been done; limited support for this version. One known issue is that you will experience random system crashes while navigating the menus. The Software Developer that MagicX hired released a second version of the Firmware that increased the CPU Clock Speed slightly, but unfortunately broke the Scraper in the process.

https://github.com/game-de-it/XU_MINI_M/releases/tag/XU_MINI_M_StockOS - Stock OS V1
<br>
https://github.com/game-de-it/XU_MINI_M/releases/tag/XU_MINI_M_StockOS_20240811 - Stock OS V2 (Increased CPU Clock, Broken Scraper)

<br>

### ~ PlumOS ~

The main Firmware available for the MiniM that is a modification of the Stock Firmware, supporting both Single Card and 2 Card Setups. Starting with version 0.4, this modification was based off of the V2 version of the Stock Firmware that broke the Scraper functionality. The DTB file that determines the Max Clock Speed of the Ram, CPU and CPU has been set to an overclock by default. Depending on the quality of the Ram in your device, this can cause your device to crash unless you replace the DTB file with one using reduced Clock Speeds. Also, for some people PPSSPP becomes broken for PSP Emulation and games will only load through Retroarch directly with lower performance; the cause of this is currently unknown.
<br>

 This firmware includes drivers for many Wifi Dongles and for some USB-C Wireless Earbuds. Overall, this is a generally usable Firmware but still has some quirks that cannot be fixed due to the project being based on the Stock Firmware. I recommend using 0.10 Stable due to additional bugs that crept into the final 1.0 version. If your system crashes or does not always boot correctly, you can replace the DTB file on your SD1 card with one of the alternate versions found on the MinUI MOSS link.

https://github.com/game-de-it/XU_MINI_M/releases/tag/plumOS_XU_MINI_M_0.10 (Download the three 0.10 Stable files and open .001 with 7zip)
<br>
https://github.com/shauninman/Moss-magicmini (Try the DTB files here if your system is unstable)

<br>

### ~ ROCKNIX ~

A Firmware based upon JELOS and has a similar feature set to PlumOS/AmberELEC, supporting both Single Card and 2 Card Setups. Has the USB Network Gadget and File Transfer Gadget(MTP) settings to transfer files via USB Cable. A stable Firmware option if you want the visual appeal of Emulation Station and the ability to use a Wifi/Ethernet USB Dongle for the Scraper or Retroachievements. Based on testing the latest May release of ROCKNIX, the Dreamcast performance is far worse compared to PlumOS and I would consider it unplayable. Also, the controller configuration for MupenN64 Standalone is incorrect and PPSSPP needs analog stick settings modified, but these are minor issues(Fixes are listed below in the RockNIX Known Issues section). 

Considering that most of the issues with this firmware are resolved, I would currently recommend it over others.

https://github.com/ROCKNIX/distribution

###### (Tests done with Bios Files, Mali GPU Drivers, CPU and GPU set to highest performance, CPU Overclock enabled)

<br>

### ~ MinUI ~

The MOSS version is based off of a cleaned/stripped version of the Stock Firmware and requires a 2 MicroSD Card setup. MinUI touts a very minimal interface for those who just want to play games without distraction and by default supports a small selection of the most popular retro consoles up to PSX. Some additional systems can be added via Pak files. The base version comes with a minor overclock, similar to PlumOS but Additional DTB files are provided in case there are any issues.

https://github.com/shauninman/Moss-magicmini (Install First)
<br>
https://github.com/shauninman/MinUI
<br>
https://github.com/ryanmsartor/XU-Mini-M-Custom-MinUI-Paks (Ry provides Additional Pak files for more systems, including Portmaster)

<br>

### ~ ArkOS ~

An early test version of ArkOS was built and is available to download on the MagicX - ArkOS Dev Discord for those who want to try it. Various Hot Keys and Buttons are not configured. PSP performance is much better and has less framerate dips than other Firmware but the button configuration is broken by default. This is only recommended for those who want to tweak and play around with an experimental OS.

Download information is available in the [#MagicX Discord Channel](https://discord.com/channels/741895796315914271/1231671960036184194/1309895866865291365)

<br>

## Customization/Themes:

Many of the existing JELOS and ArkOS themes for the 640 x 480 resolution will work across Stock, PlumOS and ROCKNIX but YMMV. The JELOS/ArkOS Theme Repository can be found here: https://github.com/Jetup13/Emulationstation-OGA-Theme-Gallery

<br>

My own Retrogirls fork of Art Book Next is also available here: https://github.com/GHROTIC/art-book-next-retrogirls-es/releases

<br>

## PlumOS Known Issues:

Q1: I've enabled the Overclock setting on PlumOS and my device is stuck in a boot loop. Do I need to re-flash?

A1: If you have access to a Linux PC to see the EXT4 partitions, you can modify the setting in STORAGE > .config/emulationstation/es_settings.cfg to:

`<string name="Overclock" value="none" />`

Otherwise you will need to reflash PlumOS.

~ <br>

Q2: Why does my Wifi Dongle not work with PlumOS?

A2: PlumOS may not have the drivers for your specific USB Dongle. The current verified USB Dongles that work with PlumOS include the TP-Link Nano AC600(Archer T2U Nano), the generic green Wifi5+BT AC600 Driver Free (8821CU), the EDUP 802.11AC Dongle(RTL88x2BU) and the MT7601 802.11n Red Background w/ White N Logo (Unknown). The images below should help you find them:
<br>

![Dongles](https://github.com/GHROTIC/xu-mini-m-guide/blob/main/assets/preview/usbdonglecombo.png)

~ <br>

Q3: How do I open the menu in Drastic(DS) on PlumOS?

A3: There is a bug where it's not using the correct configuration file for the controls. Hannah in the MagicX Discord has provided the following instructions to fix the issue:

#### Requirements
* SD Card Reader
* 7zip

#### Instructions

1. Open the PlumOS .img file in 7zip:
  * Right click > 7zip > Open Archive

2. Navigate through the archive:
  * Double click `1.img`
  * Go to `roms\gamedata\drastic\aarch64\drastic\config`
  * Drag `drastic.cfg` out and copy it

3. Access your microSD card:
  * Plug in your microSD and open the GAME partition/drive
  * If drive isn't visible, use Partition Manager to assign it a letter

4. Replace the config:
  * Navigate to `gamedata\drastic\aarch64\drastic\config`
  * Overwrite the existing `drastic.cfg` with the one from the archive

<br>

## RockNIX Known Issues:

Q1: How do I fix the controls for Mupen64 Standalone?

A1: You will have to access the main SD1 Micro SD Card with Linux, USB Network Gadget/File Transfer Gadget or SSH in with something like Filezilla. Find the Mini M Controller config(near the bottom) in /storage/.config/mupen64plus/custominput.ini and change it to:


```
[XU Mini M Gamepad]
plugged = True  
mouse = False  
AnalogDeadzone = 0,0
AnalogPeak = 22000, 22000
DPad R = button(15)
DPad L = button(14)
DPad D = button(13)
DPad U = button(12)
Start = button(9)
Z Trig = button(6)
B Button = button(3)
A Button = button(0)
C Button R = axis(3+)
C Button L = axis(3-)
C Button D = axis(2-)
C Button U = axis(2+)
R Trig = button(5)
L Trig = button(4)
Mempak switch =
Rumblepak switch =
#Analog axis configuration mappings
X Axis = axis(1-,1+)
Y Axis = axis(0+,0-)
```

~ <br>

Q2: How do I fix the Analog Stick in PPSSPP?

A2: Press the menu button and go to Settings -> Controls -> Calibrate Analog Stick. Recommended settings to change(YMMV):
```
Deadzone Radius: 0.01
Sensitivity Scale: 1.66
```
<br>

## General FAQ:

Q1: Should I purchase the MagicX Mini Zero 28 instead of the older MagicX MiniM? (UPDATED: 3-2-2025)

A1: The MagicX MiniM and the Zero 28 can be enjoyable handhelds but all versions of the current firmware have limitations for both. If you enjoy experimenting with these devices and you are able to purchase the MiniM on sale, then it may be something to consider. However, even though the cost of the Zero 28 will be higher(Aprox. $59 USD for the 64GB version), MagicX has corrected many design flaws; such as the MicroSD card protruding from the shell and risking accidental ejection. Also, in some cases the D-Pad will work properly but for many people it requires a large amount of pressure to hit a diagonal direction. 

 These issues are fixed on the Zero 28, in addition to higher quality plastic, faster processor(Allwinner A133p), 2GB of faster DDR4 1866mhz Ram, Sleep Mode, and buttons with rounded edges. The processor and ram upgrades allow the Zero 28 to run a much larger amount of the N64,  Dreamcast and PSP Libraries in a playable/enjoyable state.

 For the MagicX MiniM, most firmware development has ceased and we are limited to options that have limited features, random bugs or that require tweaks/modification to function. Due to this, the MiniM is leaning more towards Advanced Users at the current time but more Community Firmware is being worked on such as MuOS(Linux) and Knulli(Linux) that could change this in the future. 

 On the opposite side, the Stock Firmware for the Zero 28 is Android 10(Non-Touch) w/ Hotkey Navigation. For advanced users that want to add custom Android apps and modications, the hotkey based controls in addition to poor controller detection makes this a frustrating experience. For someone who wishes to just load up and play Retro Games, this is a non-issue with the Stock Firmware and makes it better suited to average users or as a gift console. Gamma Core(Android TV 13) is available for Patreon subscribers that helps fix the controller detection issues and can provide a better side loading experience, but as of Beta 3 the headset jack does not function.

~<br>

Q2: What software should I flash firmware with?

A2: Generally it's suggested to use [Rufus](https://rufus.ie/en/) if you are on Windows, as it tends to have the best success rate for flashing in general. For MacOS you are limited to something like [Balena Etcher](https://etcher.balena.io/)

~<br>

Q3: Should I use the Tape Fix on my MagicX MiniM D-Pad?

A3: Some people have had success in fixing D-Pad's with broken/poor diagonals by placing Painter's Tape under the D-Pad. Be aware that opening the shell of the MiniM will almost always break the clips used to hold the shell together. While it won't hurt the performance, the device will have seams and you may feel the shell move when pressure is applied near the edges. Examples of the fix can be found [here](https://discord.com/channels/741895796315914271/1231671960036184194/1268988801443823678) and [here](https://discord.com/channels/741895796315914271/1231671960036184194/1269305515679416450) in the #MagicX Discord Channel.

<br>


<div align="center">
  
##### Thanks to Bobby the Cat, Fishku, Gamma, Hannah, Moto, Rich, Ry, Seaninman, Snake and all in the MagicX Discord.<br>
### May the Schwartz Be With You!

</div>
