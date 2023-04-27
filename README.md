# hyprshotgun
Screenshots the way you like: Local, or online

## How to install

Arch linux users can

    yay -S hyprshotgun

If you are not on arch linux. You can clone this repository. You will need the next dependencies.

``` sh
grim slurp grimblast
```

# How to use
Check hyprland --help
``` sh
hyprshotgun display                    # Local screenshot of the active display.
hyprshotgun region                     # Locan screenshot of a region selected by the user.
hyprshotgun window                     # Locan screenshot of the active window
hyprshotgun alldisplays upload         # Local screenshot of all displays currently enabled.
```
You can upload the screenshot to an online service (https://0x0.st) by adding 'upload' at the end like in

``` sh
# The url will be copied to the clipboad!
hyprshotgun display upload
```

# I want an hyprland submap/mode!

Everything for my children
```
# BIND    MOD            KEY       DISPATCHER       VALUE
bind =    $mod SHIFT,    s,        submap,          mode_screenshot
```

```
submap=mode_screenshot

# MODE IMPLEMENTATION
# -------------------------------------

#BIND      MOD    KEY       DISPATCHER       VALUE
bind =     ,      s,        exec,            hyprshotgun upload
bind =     ,      r,        exec,            hyprshotgun region upload
bind =     ,      w,        exec,            hyprshotgun window upload
bind =     ,      d,        exec,            hyprshotgun alldisplays upload
bind =     ,      a,        exec,            hyprshotgun
bind =     ,      b,        exec,            hyprshotgun region
bind =     ,      c,        exec,            hyprshotgun window 
bind =     ,      e,        exec,            hyprshotgun alldisplays

# Exit condition
#BIND      MOD    KEY       DISPATCHER       VALUE
bind =     ,      escape,   submap,          reset 

# -------------------------------------

submap=reset
```

## Why hyprshotgun
Because it sounds rad as fuck, and the original name was [taken already](https://github.com/Gustash/Hyprshot).
