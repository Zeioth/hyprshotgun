# hyprshot
Screenshots the way you like: Local, or online

## Dependencies
You need to have installed the next packages

``` sh
grim
slurp
grimblast
```

# How to use
Check hyprland --help
``` sh
hyprshot display                    # Local screenshot of the active display.
hyprshot region                     # Locan screenshot of a region selected by the user.
hyprshot window                     # Locan screenshot of the active window
hyprshot alldisplays upload         # Local screenshot of all displays currently enabled.
```
You can upload the screenshot to an online service (https://0x0.st) by adding 'upload' at the end like in

``` sh
# The url will be copied to the clipboad!
hyprshot display upload
```

# I want an hyprland submap/mode!

Everything for my children
```
bind =    $mod SHIFT,    s,        submap,          mode_screenshot

submap=mode_screenshot

# MODE IMPLEMENTATION
# -------------------------------------

#BIND      MOD    KEY       DISPATCHER       VALUE
bind =     ,      s,        exec,             hyprshot display upload
bind =     ,      r,        exec,             hyprshot region upload
bind =     ,      w,        exec,             hyprshot window upload
bind =     ,      d,        exec,             hyprshot alldisplays upload
bind =     ,      a,        exec,             hyprshot
bind =     ,      b,        exec,             hyprshot region
bind =     ,      c,        exec,             hyprshot window 
bind =     ,      e,        exec,             hyprshot alldisplays

# Exit condition
#BIND      MOD    KEY       DISPATCHER       VALUE
bind =     ,      escape,   submap,          reset 

# -------------------------------------

submap=reset
```
