# **TIV**
### **Terminal image viewer for Linux**
\
***Requirements:***  
✣ Terminal with Unicode and 256 colors (or true color) support\
✣ imagemagick, bash, sed, bc and coreutils installed

***Usage:*** \
`tiv </path/to/image> [%zoom [±Xoffset±Yoffset]]` *(X/Y offset in characters; relative to center)*

Mode | Command
---|---
Default: | `tiv /home/user/Images/image.png`
Zoomed: | `tiv /home/user/Images/image.png` `123.456`
Zoomed & panned: | `tiv /home/user/Images/image.png` `123.456` `+13-47`
Output to file: | `tiv /home/user/Images/image.png` `> out.tiv`
Multiple output to file (animation): | `DIR="/home/user/Images"; for IMGS in $(ls $DIR); do tiv $DIR/$IMGS >> out.tiv; done` (It may create HUGE file!)
Viewing saved image/anim: | `cat out.tiv` (file can be compressed with very good compression ratio; then use `zcat` instead of `cat`)
