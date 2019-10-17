# Install Chinese Input

Here we will use IBUS, a framework of Linux input method.
 
To install IBUS pinyin, follow the steps below:

1. Upgrade package source

                sudo apt-get update

2. Go to `System Settings->Language Support->Install/Remove Languages`, tip Chinese and apply setting.

3. Generally, ubuntu 18 LTS will have IBUS installed, you can type `ibus-setup` to check it. If don't have IBUS, install as following:

                sudo apt-get install ibus ibus-clutter ibus-gtk ibus-gtk3 ibus-qt4

4. Start ibus

                im-config -s ibus

5. Install pinyin

                sudo apt-get install ibus-pinyin
    
    After installing ibus-pinyin, you should restart the computer

6. (Optional, this step is used when set the whole ibus as the input method) Setup IBUS, type `sudo ibus-setup` to open setting panel, select `input method` and add `Chinese-Pinyin`. If you don't have `Chinese-Pinyin`, try to restart the computer.

7. Go to `System Settings->Region & Language->Input Sources`, add the corresponding input method as you want.

8. Done