# awful
Awful lock screen  
  
### Features
- Other awfulness

![Imgur](https://i.imgur.com/)

### Requirements
- [i3lock-color](https://github.com/PandorasFox/i3lock-color) - i3lock fork with additional features (git)  
- [ffmpeg](https://www.ffmpeg.org/) - Screen capture  
- [xrandr](https://www.x.org/wiki/Projects/XRandR/) - Display info  
- [xdpyinfo](https://www.x.org/archive/X11R7.7/doc/man/man1/xdpyinfo.1.xhtml) - Total resolution  

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
Copy the example config to `~/.config/awful/config`. Edit.  

### Usage
Update image cache:  
```sh
awful --update PATH
```  
PATH to wallpaper image.  

Lock screen:  
```sh
awful --lock
```

Capture screen and lock:  
```sh
awful --capture
```

Lock and suspend:  
```sh
awful --suspend
```
See above.  

Additional arguments:  
```sh
awful -l -- --indicator
```

