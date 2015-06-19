# System-Heirarchy
To learn system heirarchy from basics

```
  |----------|
  | Power ON |
  |----------|
        |
        |
      \ | /
  |----------|
  |  B I O S | Basic Input Output System
  |----------|
        |
        |
      \ | /
  |----------|
  |  M B R   | Master Boot Record, also known as First Sector of Hard Disk
  |----------|
        |
        |  
      \ | /       
     /      \
    /        \     
   /   MBR    \
  / code checks\
 /  the MBR's   \      Found           |----------|
 \ partition table  _ _ _ _ _ _ _ \    |  V B R   | Volume Boot Record 
  \ for a partition               /    |----------| 
   \ set as    /                            |
    \  bootable                             |         
     \      /                               |   
      \    /                                |
Not found |                                 |
          | MBR may load a secondary boot   |
          | loader which will select a      |    
          |       partition                 |     
        \ | //_ _ _ _ _ _ _ _ _ _ _ _ _ _ __|
          |  \
  |-------------|
  | Boot Loader |
  |-------------|
        |
        |
      \ | /
  |-----------|
  |   O  S    | Operating System
  |-----------|
```

First process to start when a system is started is to load the operating system. This process is called booting. Firstly, we need to get the instruction to boot. These instructions are stored in BIOS chip.

###BIOS
The main purpose of BIOS is to load OS program. BIOS performs POST ( POWER ON SELF TEST ) for verifying all hardware components are working properly. 

  Following are the sequence of instructions that BIOS follows :-
```  
  1) Load CMOS chip : CMOS stores Computers configuration information. This information is particular to your system.
  2) Load interrupt handlers
  3) Initializes registers and power management
  4) POST
  5) Display system settings
  6) Detect bootable devices
  7) Initialize bootstrap sequence : Bootstrap sequence is to load OS.
```

###BootDevices
```
BIOS supports booting from devices such as:
a. A local hard disk drive via the Master Boot Record (MBR) (and of several MS-DOS partitions on such a disk, or GPT through GRUB 2). 
b. an optical disc drive (using El Torito).
c. a USB mass storage device (FTL-based flash drive, SD card, or multi-media card slot; hard disk drive, optical disc drive, etc.). 
d. a network interface card (using PXE).

Older, less common BIOS-bootable devices include floppy disk drives, SCSI devices, Zip drives, and LS-120 drives.

```
#### This project is under active development.
##### This project can have mistakes. Contributers are welcome.
