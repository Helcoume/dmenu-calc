# dmenu-calc
A simple dmenu calculator using `qalc`, inspired by [svenstraro's rofi-calc](https://github.com/svenstaro/rofi-calc).

[Qalculate](https://qalculate.github.io/) (qalc) is a powerful and easy to use calculator supporting complex math, many units, conversions and more...

![exemple](exemple.gif)

Exemple use `dmenu-calc -c` (`-c` is from dmenu [center](https://tools.suckless.org/dmenu/patches/center/) patch) 

The history is store in `$HOME/.local/share/dmenu-calc/history`. It is deletable (and editable if needed). To make it non-persistent, the path (`history_file`) can be changed to `/tmp/dmenu-calc/history` in the script.

# Dependencies

- [qalc](https://github.com/Qalculate/libqalculate)
- [dmenu](https://tools.suckless.org/dmenu/)
- [xclip](https://github.com/astrand/xclip)

# Installation

```bash
git clone https://github.com/Helcoume/dmenu-calc.git
```
( Optional ) Symlink to a directory in your path:
```bash
ln -s dmenu-calc/dmenu-calc /path/to/bin 
```

# Usage

Run the script with `./dmenu-calc` or `dmenu-calc` if you added it to your path.

- \<Shift-Enter\> : show the result of the current entry and copies it to the clipboard
- \<Enter\>       : copy the selected history entry to the clipboard
- \<Tab\>         : copy the selected history to the current entry
- \<Escape\>      : quit 

If no history entry matches the current entry, \<Enter\> has the behavior of \<Shift-Enter\>.

Any dmenu arguments can be used (even patch ones)

The arg `-l 10` is given by default, it can be overwritten. For example `dmenu-calc -l 2` to display only 2 lines of history.
