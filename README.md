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
- n3: Some Portmaster Games will not work due to outdated libraries. Requires additional Pak file from RY on MinUI. 
- n4: Requires Ry Pak: https://github.com/ryanmsartor/XU-Mini-M-Custom-MinUI-Paks

<br>

## Detailed notes for each OS:

### ~ Stock ~

Modified version of AmberELEC that removes many functions and options. PlumOS almost immediately replaced the stock software and little testing has been done using stock, thus there is limited support for this version. However, it is known that you will experience random system crashes when navigating the menus. The Software Developer that MagicX hired released a second version of the Firmware that increased the CPU Clock Speed slightly, while also breaking the Scraper for those who have Wifi/Ethernet Dongles.

https://github.com/game-de-it/XU_MINI_M/releases/tag/XU_MINI_M_StockOS - Stock OS V1
<br>
https://github.com/game-de-it/XU_MINI_M/releases/tag/XU_MINI_M_StockOS_20240811 - Stock OS V2 (Increased CPU Clock, Broken Scraper)

<br>

### ~ PlumOS ~

The main firmware available for the MiniM that is a modification of the Stock Firmware, supporting both Single Card and 2 Card Setups. Starting with version 0.4, this modification was based off of the V2 version of the Stock Firmware that broke the Scraper functionality. The DTB file that determines the Max Clock Speed of the Ram, CPU and CPU has been set to an overclock by default. Depending on the quality of the Ram in your device, this can cause your device to crash unless you replace the DTB file with one using reduced Clock Speeds. Overall a generally usable Firmware but still has some quirks that cannot be fixed from it being based on the Stock Firmware. Personally I recommend using 0.10 Stable due to additional bugs that crept into the final 1.0 version. If your system crashes or does not always boot correctly, you can replace the DTB file on your SD1 card with one of the alternate versions found on the MinUI MOSS link.

https://github.com/game-de-it/XU_MINI_M/releases/tag/plumOS_XU_MINI_M_0.10 (Download the three 0.10 Stable files and open .001 with 7zip)
<br>
https://github.com/shauninman/Moss-magicmini (Try the DTB files here if your system is unstable)

<br>

### ~ ROCKNIX ~

A firmware based upon JELOS and has a similar feature set to PlumOS/AmberELEC, supporting both Single Card and 2 Card Setups. More stable than PlumOS but has some strange performance issues. The main interface runs at a noticibly low framerate with no known way to resolve this. Based on repeated testing with the last two versions of the main ROCKNIX distribution, the N64 and Dreamcast performance is far worse compared to PlumOS and ArkOS. PSX and PSP are aprox the same as PlumOS performance wise, with ArkOS being the fastest and less dips for some reason. Double checked the BIOS files are in the correct location, so not really sure what's going on there.

https://github.com/ROCKNIX/distribution

<br>

### ~ MinUI ~

The MOSS version is based off of a cleaned/stripped version of the Stock Firmware and requires a 2 MicroSD Card setup. MinUI touts a very minimal interface for those who just want to play games without distraction and by default supports a small selection of the most popular retro consoles up to PSX. Some additional systems can be added via Pak files. The base version comes with a minor overclock, similar to PlumOS but Additional DTB files are provided incase there are any issues.

https://github.com/shauninman/Moss-magicmini (Install First)
<br>
https://github.com/shauninman/MinUI
<br>
https://github.com/ryanmsartor/XU-Mini-M-Custom-MinUI-Paks (Additional Pak files for more systems, including Portmaster)

<br>

### ~ ArkOS ~

An early test version of ArkOS was built and is available to download on the MagicX - ArkOS Dev Discord for those who want to try it. Various Hot Keys and Buttons are not configured. PSP performance is much better and has less framerate dips than other OS's but the button configuration is broken by default. This is only recommended for those who want to tweak and play around with an unconfigured OS.

*Ask for the link in the # MagicX Discord Channel: https://discord.gg/retrohandhelds
