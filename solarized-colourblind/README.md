# Colourblind [Solarized](https://github.com/altercation/solarized)

I tried the original Solarized colour-scheme for around 18 months to give
myself time to adjust but there were a few things I just couldn't get.  One
set of changes is to the colours to deal with my particular colour blindness,
the other is to darken the background and increase the contrast slightly.

These colours quite possibly look hideous for people with normal colour vision.
I'd recommend anyone thinking of changing the colours to try the official
variant for a fair time first.

Note that these changes don't work properly for the light variant.

## Colours

On the issue of colours, using the CIELAB value I struggle to see negative
values on the A scale.  This means that with the current colour values I
cannot see the difference between Yellow/Green, Cyan/Grey, and Violet/Blue
unless I really concentrate, and I struggle a bit with Red/Orange.

To resolve the issue of Red/Orange I brightened the Orange a little.  This
made Yellow/Orange a little ambiguous so I brightened Yellow as well.  This
breaks the light variant of Solarized since yellow is now too bright.

Green I shifted further negative on the A scale and darkened slightly.

Violet I shifted significantly positive on the A scale and brightened slightly.

Cyan I had to shift negative on the B scale (i.e. add some blue) since no
amount of added green made any difference for me.  I also darkened it
slightly.

The blue value is slightly changed because the CIELAB -> Hex converters I
could find have a different value to what is in the original Solarized tables.

Overall the changes in brightness (with the exception of Yellow) have brought
the colours within the 45-55 range that I now use for typical values in the
grey-scale values.

## Contrast

I struggle to see a difference of 5 points of Luminance in the CIELAB scale so
I have moved the grey-scale values to increase the values a little.  I also
didn't like how bright the BASE03 value was.  This change has overall created
one incompatibility, and that is that I have swapped the roles of the BASE00
and BASE01 values since I felt BASE01 was too dark to be used in general for
"secondary content".

BASE00 should in general not be used, but in the few places where it has been
in the VIM syntax highlighting file I have either swapped it with BASE01 or
emboldened it (which only helps if you have a bold font).

## Tabled Values

    SOLARIZED HEX      L*A*B
    --------- -------  ----------
    base03    #001721   5 -12 -12
    base02    #002b36  15 -12 -12
    base00    #375760  35 -09 -09
    base01    #586e75  45 -07 -07
    base0     #73878c  55 -06 -05
    base1     #93a1a1  65 -05 -02
    base2     #d2ccb9  87  00  10
    base3     #fdf6e3  97  00  10
    yellow    #ca9519  65  10  65
    orange    #df5922  55  50  55
    red       #dc322f  50  65  45
    magenta   #d33682  50  65 -05
    violet    #ba5dd3  55  55 -45
    blue      #008dd1  55 -10 -45
    cyan      #0095ae  55 -35 -25
    green     #589300  55 -40  65

