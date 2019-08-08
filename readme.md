### cliphist

*clipboard history "manager" for wayland*

- synchronise your two clipboards (primary and the other one)
- write changes in either to a history file (reset on boot)
- recall history with dmenu (for example)

required: [wl-clipboard-rs](https://github.com/YaLTeR/wl-clipboard-rs) or [wl-clipboard](https://github.com/bugaevc/wl-clipboard)

### usage

###### start the daemon

`$ cliphist listen`  
this will listen for changes on either clipboard, make sure they're in sync, and write to the history.  
call it once per session - for example in your sway config

###### select old item

`$ cliphist select | dmenu -l 10 | cliphist copy`  
bind it to something nice on your keyboard
