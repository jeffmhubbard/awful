# awful
Awful lock screen  

### Features
- Mostly themeable
- Generates images with various effects
- Multi-monitor support
- Other awfulness

### Requirements
- [i3lock-color](https://github.com/PandorasFox/i3lock-color) - i3lock fork with additional features( >= 2.11-c ).
- [imagemagick](https://www.imagemagick.org/script/index.php) - To apply effects to images.
- [xrandr](https://www.x.org/wiki/Projects/XRandR/) - Get display info.
- [xdpyinfo](https://www.x.org/archive/X11R7.7/doc/man/man1/xdpyinfo.1.xhtml) - Get total resolution.
- [xrdb](https://www.x.org/pub/X11R7.5/doc/man/man1/xrdb.1.html) - Custom DPI support.
- [bc](https://www.gnu.org/software/bc/) - Do math.

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
Copy the example config to `~/.config/awfulrc`. Example is kinda commented...  

### Usage
- Update image cache: `awful -u PATH` PATH can be a single image or directory. If PATH is a directory, a random image will be selected.  
- Lock screen: `awful -l [EFFECT]` EFFECT can be dim, blur, dimblur, pixel or blank.  
- Lock and suspend: `awful -s [EFFECT]` See above.  

