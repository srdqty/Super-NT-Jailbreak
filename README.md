# Super NT Jailbreak

Custom "*Jailbreak*" firmware for the [Analogue Super
NT](https://www.analogue.co/pages/super-nt/) that allows loading ROMs
from the SD Card slot and an expanded featureset. 

## Updating Firmware 

Format a 2GB (or larger) SD card as
[FAT32](https://en.wikipedia.org/wiki/FAT32) (FAT16 and exFAT are not
supported). In Windows, you must use a tool for cards larger than
32GB, such as
[fat32format](http://www.ridgecrop.demon.co.uk/index.htm?guiformat.htm).

Place the firmware file
[snt_firmware_verJB6.5.bin](https://github.com/SmokeMonsterPacks/Super-NT-Jailbreak/releases/download/v6.5/snt_firmware_verJB6.5.bin)
into the root directory of your SD card.  Be sure that there is only
one firmware file there.  Insert the card into your Super NT and power
it on. The firmware will be flashed to the console.

The console LED will turn red and flicker while the firmware is flashed.
This process may take a few minutes.  The main menu will load when it 
finishes.  Delete the firmware file from your SD card after flashing.

## Organizing ROMs

Create a folder called `SNES` at the root of your SD card, and drop
your folders and subfolders of ROMs inside (see [SmokeMonster's
database](https://github.com/SmokeMonsterPacks/EverDrive-Packs-Lists-Database)
for a curated [list of valid SNES
ROMs](https://github.com/SmokeMonsterPacks/EverDrive-Packs-Lists-Database/raw/master/EverDrive%20Pack%20SMDBs/Super%20EverDrive%20%26%20SD2SNES%20SMDB.txt)).
The system will search for ROMs in the `/SNES/` folder first, or the
root directory of the SD card if there is no `/SNES/` folder.  The
maximum number of files (ROMs and subfolders) that can be placed in a
given folder is around 300-500, depending on the length of the
filenames.

## Running ROMs

Select **browse SD card** from the main menu.  Hit **enter** on a
filename to run it, or if it's a subfolder, it will enter said folder.
The menu hotkey will return to the file menu from the game.

## Saves

Saves will go into `/SAVES/SNES/` by default.  You can directly place
an [SD2SNES](http://sd2snes.de/) or [Super
Everdrive](https://krikzz.com/store/home/13-super-everdrive-v2.html)
SD card in, and it will properly detect this by checking for the
requisite save game folders, in this order:

- `/SAVES/SNES/` (default)
- `/SPED/SAVE/` (Super EverDrive)
- `/sd2snes/saves/` (SD2SNES)

The Super Everdrive uses a 32-kilobyte long save file no matter what,
and is padded.  This functionality is retained.  It should be possible
to swap your SD card into the unit from your SD2SNES or Super
EverDrive and the saves will work fine, then it can be put back into
said cartridge and it will find the updated saves (with a `.sav` file
extension, other extensions are not recognized).

It is a good idea to backup your saves before using this firmware.

When the game is exited back to the menu, it will prompt you to save.  
So to save your progress, be sure to return to the file menu before 
turning the system off.

## Cores Supported

`SNES/SFC`

## Changelog

- [JB6.5](https://github.com/SmokeMonsterPacks/Super-NT-Jailbreak/releases/download/v6.5/snt_firmware_verJB6.5.bin) 2018-03-04:
  - includes all fixes from official firmware v4.4, which should
    solve most DMA-related random crashes
  - adds a `menu bounce` option (reinstated)
  - adds a new `Save?` dialog box
  - fixes both SRAM bugs (firmware 6.4 only saved once and had a nasty
    corruption bug). Please test it again so we can be sure the save
    functionality works as expected. Any save made on the jailbreak
    firmware 6.4 should be considered as potentially corrupted and
    must be discarded
  - fixes glitch with some games disabling the `return to menu`
    shortcut
    
- [JB6.4](https://github.com/SmokeMonsterPacks/Super-NT-Jailbreak/releases/download/v6.4/snt_firmware_verJB6.4.bin) 2018-02-14 Initial release: Happy Valentine's Day :heart:

## Problem Reporting and Community chat

The custom firmware is not coded by
[SmokeMonsterPacks](https://github.com/SmokeMonsterPacks) or
[frederic-mahe](https://github.com/frederic-mahe), but please do
report problems here at Github for support. Priority will be given to
jailbreak-specific problems (using ROMs through the SD card slot
rather than through the cartridge slot). You can join the [discord
server](https://discord.gg/EX57xnF) if you want to chat with the Super
Nt community.
