use weston

stacking compositor with an official package

seems more lightweight than the other ones that are part of a desktop environment

weston also has a text config file

https://wiki.archlinux.org/title/Weston

weston needs gnu-free-fonts package in order to not have squares in the title bar of the terminal
but, gnu-free-fonts is not a dependency. why is that? can this be avoided by choosing a different font in the weston config?

the weston arch wiki page does mention shell fonts. it says it uses the "default sans-serif font" for window titles, etc. and gives some tips on how to change the font. 
so, it's possible that gnu-free-fonts is simply a missing dependency but arch by default has a really awesome font so i'd rather use that
