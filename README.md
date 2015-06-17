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

```
  Following are the sequence of instructions that BIOS follows :-
  
  1) Load CMOS chip : CMOS stores Computers configuration information. This information is particular to your system.
  2) Load interrupt handlers
  3) Initializes registers and power management
  4) POST
  5) Display system settings
  6) Detect bootable devices
  7) Initialize bootstrap sequence : Bootstrap sequence is to load OS.
```
#### This project is under active development.
#### Contributers are welcome
