# Windows 98 Second Edition Install Guide

- If you are experiencing hardware instabilities such as being unable to run at full CPU clock speed. Install Windows 9x without ACPI by forcing APM mode with ```setup.exe /p i```

- Tweak BIOS settings to your liking before installing Windows.

- If sound doesn't work in some games it can be because some Windows games use WDM drivers instead of VXD drivers.

- If you are having errors booting into floppy and CD media, reset the BIOS settings.

- Keep partition size under what OS and hardware can support.
  - It is recommended to have a 32GB partition but Windows 95 OSR 2.5, 98 & ME supports up to 137GB partitions natively.

- Instead of configuring boot loader for dual booting, have operating systems on their own seperate drive. Then boot into them by marking unused drives to not installed.
  - BIOS → IDE HDD AUTO-DETECTION → UNUSED DRIVES → NOT INSTALLED

- Note on audio drivers, VXD DRIVERS WILL PERFORM BETTER IN DOS GAMES AND YOU CAN REBOOT INTO MS-DOS WITH VXD DRIVERS WDM DRIVERS WORK ONLY ON DOS GAMES RUNNING ON WINDOWS BUT ALSO WORK WITH WINDOWS GAMES SUCH AS USNF 97 AND FIGHTERS ANTHOLOGY BUT YOU WON'T BE ABLE TO REBOOT INTO MS-DOS WITH WORKING SOUND VIA WDM DRIVERS. WDM DRIVERS PERFORM WORSE THAN VXD BUT PROVIDES MORE COMPATIABLITY WITH WINDOWS AND DOS GAMES.

CHOOSE WDM DRIVER FOR COMPATIBILITY WITH GAMES
# Recommended BIOS Settings:
```
- LOAD SETUP DEFAULTS - LOADS PERFORMANCE SETTINGS
- LOAD BIOS DEFAULTS - ONLY FOR TROUBLESHOOTING
- ADJUST TIME
- BOOT ORDER - AS NECESSARY
- USB KB/MOUSE LEGACY - KEYB + MOUSE (IF USING ONE)
- PnP AWARE OS - ON
- PRIMARY GRAPHICS ADAPTER - AGP (IF RUNNING AGP VIDEO CARD)
- COMPLIANCE WITH O/S - NO (FORCE APM INSTALL)
- UNUSED PORTS (SERIAL, PARALLEL, etc) - DISABLED
- ONBOARD AC’97, LEGACY AUDIO & SOUND BLASTER - DISABLED
- FSB SPEED - (ADJUST AS NECESSARY) - FOR ME I HAVE A PENTIUM III 1000MHZ AND IT RUNS GREAT AT A FSB OF 133MHZ.
- VOLTAGE - (ADJUST AS NECESSARY FOR PROCESSOR)
- IDE HDD AUTO DETECTION - SELECT (TO REFRESH DRIVES)
```

# Pre-Installation Procedures:
- Make sure hard drive isn't slave to CD-ROM
- I use [SeaTools](https://www.seagate.com/support/downloads/seatools/seatools-legacy-support/) and [WD Data Lifeguard Tools](https://www.philscomputerlab.com/western-digital.html) to format the partitions instead of using ```fdisk``` for quicker formats. By not using ```fdisk```,you don't get sector checks like you would when creating and formating partitions in fdisk.
- If installing on a Seagate hard drive
  - Use SeaTools to reset disk size or cap partition to 32GB.
  - Then use [Seagate DiscWizard Starter Edition](https://www.philscomputerlab.com/seagate.html) to configure the rest of the drive.
- If installing on a Western Digital hard drive
  - Insert EZ-Drive floppy diskette.
    - If there are boot floppy errors, reset the BIOS settings and set it to the lowest processor speed and physically disconnect other drives.

# Basic CLI Commands: 
- ```cd``` - Change directory.
- ```cd\``` - Goes back to previous directory.
- ```dir``` - Shows every file in the directory.
- ```dir /p``` - Loads all the files one screenful at a time.
- ```dir /w``` - Loads information widefully.
- ```copy *.* c:\``` - Common way to copy files. 
- ```format a: /u``` - Low level format floppy diskettes.
- ```format c: /q /u /s``` - Use this command if you cannot format drive after using fdisk on it. Go to the CD-ROM, cd into win98 folder, and run the command.
- Resetting HDD to factory settings: [https://www.youtube.com/watch?v=rGSjWwTy1Rg](https://www.youtube.com/watch?v=rGSjWwTy1Rg)

# Standard Installation Procedures:
- Boot with Windows 98 Second Edition Boot Disk
- Start computer with CD-ROM support
- Make directory on C: drive with “md win98”
- Go to CD-ROM and ```cd``` into win98 folder
- Run ```copy *.* C:\win98``` (copies installation files to hard drive directly and Windows won't nag you to insert disk when updating drivers)
- Go to C drive and run ```setup.exe /p i``` ("/p i" parameter bypasses the reporting the existence of a Plug and Play BIOS during setup).
- Running setup.exe /p j forces Windows to use ACPI/PnP (Useful if having a newer ACPI BIOS not recognized)

# Post install housekeeping
- Add or remove Windows features, if not done already during installation process.

- Verify DMA Mode is turned on for Storage & CD-ROM in Device Manager
  - If unstable disable DMA mode  

- Set sound output for devices in multimedia to have the highest sample rate conversion quality

- Set file system in Settings → System → Performance → File System → Network Server 

- Remove network login prompt by going to ```Settings → Network → Primary Network Logon → Windows Logon```
  - If you didn't have a Windows password, it should boot into the desktop directly
  
# Optional 9x Updates
- **Windows 98 SE Update CD** - https://archive.org/details/w98se-upd-r1

- **Windows ME Update CD** - https://archive.org/details/wmeupd-r2
  - An unoffical package containing all the offical updates ever released for Windows ME. 

# Windows 9x Tips:
- If having issues with USB drives, try formatting within Windows 9x.
- If burning disks make sure burn speed is slow like 10X and verifying the content is burnt in ISO 9660 file system.
- Installing the DirectX version your graphics card supports is recommended, but you may want to stick to installing DirectX 7.0a for more period correct games.
- If dual booting XP and using EZ-Drive make sure FAT32 partition for 98 is smaller than the NTFS partition for XP.
- https://www.reddit.com/r/windows98/comments/1d26gr7/here_is_a_actual_network_sharing_fix_for_windows/

# Recommended Software & Websites
- **3DMark** - https://www.philscomputerlab.com/futuremark-3dmark.html
- **86Box** - https://86box.net/
- **Audigy 2 ZS** - https://www.vogons.org/viewtopic.php?f=62&t=71449
- **DAMEON Tools** - https://www.philscomputerlab.com/daemon-tools-windows-98.html
- **Diskeeper 6.0** - https://winworldpc.com/product/diskeeper/60
- **ImgBurn** - https://www.imgburn.com/
- **Legacy DirectX Versions** - http://falconfly.3dfx.pl/directx.htm
- **Legacy Update** - https://legacyupdate.net/
- **MemTest86** - https://www.memtest86.com/index.html
- **Microsoft Plus!** - https://winworldpc.com/product/plus/1998
- **Norton Ghost 2003** - https://archive.org/details/norton_ghost_2003/
- **Phils Computer Lab** - https://www.philscomputerlab.com/
- **Sidewinder 3D Pro Drivers** - https://www.vogons.org/viewtopic.php?t=63181
- **VIA Chipset Drivers** - https://www.georgebreese.com/net/software/
- **Windows CD Emulator** - https://wincdemu.sysprogs.org/download/
- **Windows Installer 2.0** - https://archive.org/details/instmsi   
- **Windows Update Restored** - http://windowsupdaterestored.com/
- **WinImage** - https://winworldpc.com/product/winimage/61
- **WinWorldPC** - https://winworldpc.com/library/operating-systems

# DOSBox tips: 
- Mounting directory - ```mount C (path of directory)```
- Mounting CD drive - ```mount (drive letter) (letter of CD-ROM) -t CDROM```
- Mounting ISO - ```imgmount “drive letter” “path to iso.iso” -t iso```
- Mounting CUE/BIN files - ```imgmount (drive letter) (path to cue.cue) -t iso```

To use joystick in DOSBox configure the config file in the install by changing ```JOYSTICK=AUTO``` to ```JOYSTICK=CH```, and ```SWAP34=TRUE``` then set the joystick in the game to ```CH JOYSTICK```then calibrate.
```
JOYSTICKTYPE=CH
TIMED=TRUE
AUTOFIRE=FALSE
SWAP34=TRUE
BUTTONWRAP=FALSE
```

# Windows Keys
- **Windows 95** - 29696-OEM-0015933-60761
- **Windows 98 SE** - G2FGT-6HYRW-X2W2C-RT7HW-RF7WX
- **Windows ME** - TH3RK-MQC86-YX3PH-8DC4R-RKQ72

# References
- https://www.vogons.org/viewtopic.php?f=61&t=52119
- https://www.vogons.org/viewtopic.php?p=1034545
