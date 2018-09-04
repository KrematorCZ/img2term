# **img2term**
### **Linux terminal image viewer**
\
***Requirements:***  
✣ Terminal with Unicode and 256 colors (or true color) support\
✣ imagemagick, bash, sed, bc and coreutils installed

***Usage:*** \
`img2term </path/to/image> [%zoom [±Xoffset±Yoffset]]` *(X/Y offset in characters; relative to center)*

Mode | Command
---|---
Default: | `img2term /home/user/Images/image.png`
Zoomed: | `img2term /home/user/Images/image.png` `123.456`
Zoomed & panned: | `img2term /home/user/Images/image.png` `123.456` `+13-47`
Output to file: | `img2term /home/user/Images/image.png` `> out.ti`
Multiple output to file (animation): | `DIR="/home/user/Images"; for IMGS in $(ls $DIR); do img2term $DIR/$IMGS >> out.ti; done` (It may create HUGE FILE!)
Viewing saved image/anim: | `cat out.ti` (file can be compressed with very good compression ratio; then use `zcat` instead of `cat`)
