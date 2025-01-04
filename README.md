<div align="center">
  
  # **-== Xu Mini M Guide==-**

</div>

<br>
  
### ~ Quick Comparison Table of OS Features: ~

</div>

| - | Stock | PlumOS | Rocknix | MinUI(MOSS) |
| -- | -- | -- | -- | -- |
| Scraper*(n0): | Yes/No*(n1) | No(Broken) | Yes | No |
| Game Switcher: | No | No | No | No |
| Boot to Game: | No | No | Partial*(n2) | No |
| Portmaster: | No | Yes*(n3) | Yes | Yes*(n3) |
| Dreamcast: | ? | Fair | Poor | N/A |
| N64: | ? | Fair | Poor | Fair*(n4) |
| PSP: | ? | Fair | Fair | N/A |
| PSX: | ? | Good | Good | Good |


###### (Ratings Scale based on: Poor->Fair->Good->Very Good->Excellent)
- n0: Scraper Requires compatible Wifi or Ethernet USB Dongle. Dongle compatability varries based on OS. 
- n1: Scraper is working on Stock Firmware V1 but broken on Stock Firmware V2.
- n2: Rocknix has the option to immediately open a game and continue at the last auto save state when opening a rom file (Retroarch Only).
- n3: Some Portmaster Games will not work due to outdated libraries. Requires additional Pak file from Ry to support Portmaster on MinUI. 
- n4: Requires Ry Pak: https://github.com/ryanmsartor/XU-Mini-M-Custom-MinUI-Paks

<br>

## Notes for each OS:

### ~ Stock ~

Modified version of the AmberELEC Firmware that removes many functions and settings. PlumOS almost immediately replaced this Stock Firmware and little testing has been done; limited support for this version. One known issue is that you will experience random system crashes while navigating the menus. The Software Developer that MagicX hired released a second version of the Firmware that increased the CPU Clock Speed slightly, but unfortunately broke the Scraper in the process.

https://github.com/game-de-it/XU_MINI_M/releases/tag/XU_MINI_M_StockOS - Stock OS V1
<br>
https://github.com/game-de-it/XU_MINI_M/releases/tag/XU_MINI_M_StockOS_20240811 - Stock OS V2 (Increased CPU Clock, Broken Scraper)

<br>

### ~ PlumOS ~

The main Firmware available for the MiniM that is a modification of the Stock Firmware, supporting both Single Card and 2 Card Setups. Starting with version 0.4, this modification was based off of the V2 version of the Stock Firmware that broke the Scraper functionality. The DTB file that determines the Max Clock Speed of the Ram, CPU and CPU has been set to an overclock by default. Depending on the quality of the Ram in your device, this can cause your device to crash unless you replace the DTB file with one using reduced Clock Speeds. 
<br>

Overall, this is a generally usable Firmware but still has some quirks that cannot be fixed due to the project being based on the Stock Firmware. I recommend using 0.10 Stable due to additional bugs that crept into the final 1.0 version. If your system crashes or does not always boot correctly, you can replace the DTB file on your SD1 card with one of the alternate versions found on the MinUI MOSS link.

https://github.com/game-de-it/XU_MINI_M/releases/tag/plumOS_XU_MINI_M_0.10 (Download the three 0.10 Stable files and open .001 with 7zip)
<br>
https://github.com/shauninman/Moss-magicmini (Try the DTB files here if your system is unstable)

<br>

### ~ ROCKNIX ~

A Firmware based upon JELOS and has a similar feature set to PlumOS/AmberELEC, supporting both Single Card and 2 Card Setups. A stable Firmware option if you would like to use a Wifi/Ethernet USB Dongle for the Scraper or Retrachievements. Oddly the main User Interface runs at a noticibly low framerate with no known way to change this in the settings. Based on repeated testing with the last two versions of the main ROCKNIX distribution, the N64 and Dreamcast performance is far worse compared to other Firmware; PSX and PSP perform aproximately the same. This Firmware may be a good option if you have no plans to play any N64 or Dreamcast titles.

https://github.com/ROCKNIX/distribution

###### (Tests done with Bios Files, Mali and Panfrost GPU Drivers, CPU and GPU set to highest performance, CPU Overclock enabled)

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

An early test version of ArkOS was built and is available to download on the MagicX - ArkOS Dev Discord for those who want to try it. Various Hot Keys and Buttons are not configured. PSP performance is much better and has less framerate dips than other OS's but the button configuration is broken by default. This is only recommended for those who want to tweak and play around with an unconfigured OS.

Download information available in the [#MagicX Discord Channel](https://discord.com/channels/741895796315914271/1231671960036184194/1309895866865291365)

<br>

## Customization/Themes:

Many of the existing JELOS and ArkOS themes for the 640 x 480 resolution will work across Stock, PlumOS and ROCKNIX but YMMV. The JELOS/ArkOS Theme Repository can be found here: https://github.com/Jetup13/Emulationstation-OGA-Theme-Gallery

<br>

My own Retrogirls fork of Art Book Next is also available here: https://github.com/GHROTIC/art-book-next-retrogirls-es/releases
