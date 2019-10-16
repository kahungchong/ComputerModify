# SpaceFn for windows

## Introduction

Actually it is a script of AutoHotKey, which is used for automation scripting on windows. Therefore it will have two steps to apply SpaceFn, download and install AutoHotKey first and then run the script.

## Procedure

1. Download and install [AutoHotKey](https://www.autohotkey.com/)
2. Download all the files in `spacefn-win` folder and then double click `spacefn-win` to run the script and Done. Very simple.
3. You can also modify the script as you want, whose syntax is easy. There are several predefined mapping modes about arrow keys, you can easily switch among different modes by modifying line 9, or even create your own style.

## Switch CapsLock and Left-Ctrl

Somebody may want to switch capslock and left-ctrl as capslock key locates in one of best spots on keyboard but with less usage. To let caps lock die, we should modify regedit as following:

1. Click `Win+R`
2. Input `regedit` to open regedit
3. Enter `HKEY_LOCAL_MACHINE -> System -> CurrentControlSet -> Control -> KeyBoard Layout`
4. Right click and select `New -> Binary value`
5. Rename the new created file (named `New Value #1` by default) to `Scancode Map`
6. Right click on the renamed file and select `Modify`
7. Then input as following:

                0000 00 00 00 00 00 00 00 00 
                0008 03 00 00 00 1D 00 3A 00 
                0010 3A 00 1D 00 00 00 00 00 
                0018

8. The final step, restart the computer and it will take effect.