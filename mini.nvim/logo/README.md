Code to convert pixel logos to logos with width of 800 pixels:

```
convert logo_*_pixels.gif -filter point -set filename:fn '%[basename]-big' -resize 800x^1 '%[filename:fn].png'
# Then bulk rename 'logo_xxx_pixels-big.gif' into 'logo_xxx.gif'.
```

Code to conver pixel logos to logos with size 1280x640 pixels and same aspect ratio but transparent padding (for Github social preview):

```
convert logo_*_pixels.gif -filter point -background none -resize 1280x^1 -gravity center -extent 1280x640 -set filename:fn '%[basename]-github' '%[filename:fn].png'
# Then bulk rename 'logo_xxx_pixels-github.gif' into 'logo_xxx_github.gif'.
```
