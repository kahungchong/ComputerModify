- Map arrow key to space + edfs
    - Download and install [xcape](https://github.com/alols/xcape)

    - Check keycode of keys want to modify
        Use `xev` command in terminal

    - Modify `~/.Xmodmap`
        [Mannual](https://www.zouyesheng.com/xmodmap-usage.html) of Xmodmap.

        Syntax: `keycode{a} = {single_click_a shift+a mode_switch+a}`

        Add the following mapping codes:

                keycode 65 = Mode_switch space space space
                keycode anykey = space

                keycode 39 = s S Left
                keycode 40 = d D Down
                keycode 26 = e E Up
                keycode 41 = f F Right

    - Implement change

                xmodmap ~/.Xmodmap && xcape -e '#65=space' -t 250
        

