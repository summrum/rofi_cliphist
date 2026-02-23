# Rofi cliphist Mode
A Rofi cliphist mode that shows icons for images and hides clipboard entry ID.
![example of cliphist mode](https://github.com/summrum/rofi_cliphist/blob/main/rofi_cliphist_example.png?raw=true)
## Requirements:
**POSIX shell**  
**Rofi** window switcher/application launcher/dmenu replacement  
**cliphist** wayland clipboard manager with support for multimedia  
**wl-clipboard** command-line copy/paste utilities for wayland  
## Usage:
Ensure script is executable, then use one of the following options to add to your Rofi modi:  

**Option 1:** Launch Rofi with a script mode set using the syntax ```"{name}:{executable}"```  
```
rofi -show clipboard -modi "clipboard:/path/to/script/rofi_cliphist"
```
**Option 2:** Add custom mode to Rofi ```config.rasi``` file  
```
configuration {
	modi: "clipboard:/path/to/script/rofi_cliphist";
}
```
Other modi can be added as usual seprarated by commas; the mode also doesn't have to be called "clipboard", any name or glyph can be used.  

The clipboard mode should then be available when launching Rofi, offering a list of clipboard data. Selecting any option will copy the data and close Rofi, ready for the data to be pasted. Using the "delete-entry" key combination will delete the selected item (e.g. pressing Shift+Delete if using default keyboard configuration will delete highlighted item). 
