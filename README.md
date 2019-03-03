# awful
Awful lock screen  
  
Another wrapper script for i3lock. It's based on
[betterlockscreen](https://github.com/pavanjadhaw/betterlockscreen), so the
same concept applies -- cache wallpaper, apply effects, and create background
for the indicator.

### Features
- Multi-monitor support with image spanning
- Centered indicator with time, date, and keyboard layout
- Apply several different image effects: dim, blur, pixel, morph
- All effects are optional to speed up image caching
- Less arguments, more config
- Other awfulness

![Imgur](https://i.imgur.com/y1cpYv7.png)

### Requirements
- [i3lock-color](https://github.com/PandorasFox/i3lock-color) - i3lock fork with additional features (git)  
- [imagemagick](https://www.imagemagick.org/script/index.php) - To apply effects to images  
- [xrandr](https://www.x.org/wiki/Projects/XRandR/) - Get display info  
- [xdpyinfo](https://www.x.org/archive/X11R7.7/doc/man/man1/xdpyinfo.1.xhtml) - Get total resolution  
- [xrdb](https://www.x.org/pub/X11R7.5/doc/man/man1/xrdb.1.html) - Use Xft.dpi 
- [bc](https://www.gnu.org/software/bc/) - Do math  

### Installation
```sh
git clone https://github.com/jeffmhubbard/awful
cd awful
sudo install -Dm 755 awful /usr/bin/awful
```

##### For suspend with systemd
```sh
sudo install -Dm 644 awful@.service /usr/lib/systemd/system/awful@.service
sudo systemctl daemon-reload
sudo systemctl enable awful@$USER.service
```

### Configuration
Copy the example config to `~/.config/awfulrc`. Edit.  

### Usage
Update image cache:
```sh
awful -u PATH
```  
PATH can be a single image or directory. If PATH is a directory, a random image will be selected.  

Lock screen:
```sh
awful -l EFFECT
```
EFFECT can be dim, blur, pixel or morph. No EFFECT will use normal image or $defaltfx if set. 

Lock and suspend:
```sh
awful -s EFFECT
```
See above.  

Additional arguments:
```sh
awful -l -- --indicator
```

