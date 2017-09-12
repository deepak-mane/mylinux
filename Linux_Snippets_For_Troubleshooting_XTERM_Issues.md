# mylinux


# LINUX SNIPPETS FOR 

## TO xterm font tweak to supress and fix a font error


error message before
xterm: cannot load font '-misc-fixed-medium-r-semicondensed--13-120-75-75-c-60-iso10646-1'

you need to make a 
.Xdefaults file in your $HOME 

to keep it simple here is what I used to test with the contents of .Xdefaults 

updated .Xdefaults from info at arch
```linux
xterm*geometry:           80x25
xterm*faceName:           terminus:bold:pixelsize=14
xterm*dynamicColors:      true
xterm*utf8:               2
xterm*eightBitInput:      true
xterm*saveLines:          512
xterm*scrollKey:          true
xterm*scrollTtyOutput:    false
xterm*scrollBar:          true
xterm*rightScrollBar:     true
xterm*jumpScroll:         true
xterm*multiScroll:        true
xterm*toolBar:            false
```
run

```linux
fc-cache

xrdb -merge ~/.Xdefaults

xterm  -geometry 70x24
```