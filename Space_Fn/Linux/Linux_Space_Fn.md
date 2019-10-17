# Linux_Space_Fn

## Procedure
1. Download and install [xcape](https://github.com/alols/xcape)

2. Check keycode of keys want to modify
        Use `xev` command in terminal

3. Modify `~/.Xmodmap`
        
    [Mannual](https://www.zouyesheng.com/xmodmap-usage.html) of Xmodmap.

    If there is no `.Xmodmap`, just create one by yourself.



        Syntax: `keycode{a} = {single_click_a shift+a mode_switch+a}`

        Add the following mapping codes:

                keycode 65 = Mode_switch space space space
                keycode anykey = space

                keycode 39 = s S Left
                keycode 40 = d D Down
                keycode 26 = e E Up
                keycode 41 = f F Right

4. Implement change

                xmodmap ~/.Xmodmap && xcape -e '#65=space' -t 250

## Switch Capslock and left ctrl

Switch capslock and left ctrl, and make capslock to switch input method

1. Install gnome
                sudo apt-get install gnome

2. Restart computer and choose gnome when login

3. Open gnome-tweaks
                gnome-tweaks

4. Go to `Keyboard & Mouse->Additional Layout Options`, tip the following options:

    - `Ctrl Position -> Cpas Lock as Ctrl`
    - `Switching to another layout -> Left Ctrl`

    If you just want to switch capslock and left ctrl, it also has option for switching them only.

## Apperances for gnome
[MacOS style](https://zhuanlan.zhihu.com/p/37852274)

## Scale on 4k screen

1. `xrandr` to see monitor version
2. `xrandr --output DP-2 --scale 0.6x0.6`, where `DP-2` is name of monitor

        

