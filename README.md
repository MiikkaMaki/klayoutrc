# klayoutrc
KLayout resources file for my configurations.

## How to use
When you open KLayout with environment variable `KLAYOUT_HOME` pointing to a directory, KLayout will try to fetch the `klayoutrc` file from this directory. If the file does not exist, it will create it. When you change KLayout settings from the GUI, it will save the settings to this file.

To use this provided `klayoutrc`, you can:

1. Move this to the directory where your `KLAYOUT_HOME` is pointing to, or
2. copy and paste these settings in the next codeblocks to your own `klayoutrc` file so you don't have to lose any existing settings.

## Settings included

+ Dark background color for friends of the dark Magic:

```
 <background-color>#000000</background-color>
```

+ Make `edit mode` (`klayout -e`) default:
    + Read only can still be used with `klayout -ne`.
```
 <edit-mode>true</edit-mode>
```

+ See all hierarchy levels as default:
```
 <full-hierarchy-new-cell>true</full-hierarchy-new-cell>
```

+ Disable hints:
```
 <tip-window-hidden>editor-mode=4,editor-mode=0,only-top-level-shown-by-default=3</tip-window-hidden>

```

+ Key-bindings that may be more intuitive:
```
 <key-bindings>
edit_menu.clear_all_rulers:'Shift+K';
edit_menu.mode_menu.box:R;
edit_menu.mode_menu.instance:I;
edit_menu.mode_menu.move:M;
edit_menu.mode_menu.path:P;
edit_menu.mode_menu.ruler:K;
edit_menu.mode_menu.text:L;
file_menu.save:'Ctrl+S';
zoom_menu.zoom_fit:F;
zoom_menu.zoom_out:'Shift+Z';
zoom_menu.select_current_cell:'Ctrl+0';
</key-bindings>
```

## Some notes
+ This configure file has been created using KLayout 0.30.5 on ubuntu, I don't know for sure if the versions have differences.
+ Change for `save` to be `Ctrl+S` required change of a default key-binding for `select current_cell`, so it is now set to `Ctrl+0`. For some reason KLayout did not allow it to be none.
