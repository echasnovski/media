Code to convert pixel logos to logos with width of 800 pixels:

```
convert logo_xxx_pixels.gif -filter point -set filename:fn '%[basename]-big' -resize 800x^1 '%[filename:fn].png'

# Rename 'logo_xxx_pixels-big.png' into 'logo_xxx.png'.
mv logo_xxx_pixels-big.png logo_xxx.png
```

Code to convert pixel logos to logos with size 1280x640 pixels and same aspect ratio but transparent padding (for Github social preview):

```
convert logo_xxx_pixels.gif -filter point -background none -resize 1280x^1 -gravity center -extent 1280x640 -set filename:fn '%[basename]-github' '%[filename:fn].png'

# Rename 'logo_xxx_pixels-github.png' into 'logo_xxx_github.png'.
mv logo_xxx_pixels-github.png logo_xxx_github.png
```
