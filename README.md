# awful

Awful lock screen; another i3lock wrapper  
  
![Lock](https://i.imgur.com/t7Qwq7w.png)
Lock with cached image

![Capture](https://i.imgur.com/0LoVkLn.png)
Lock with screen capture

### Features
- Cache image with blur and vignette effects
- Capture screenshot with blur and vignette effects
- Lock screen

### Requirements
- [i3lock-color (git)](https://github.com/PandorasFox/i3lock-color) - i3lock fork with additional features  
- [ffmpeg](https://www.ffmpeg.org/) - Image effects and screen capture  
- [xrandr](https://www.x.org/wiki/Projects/XRandR/) - Display info  
- [xdpyinfo](https://www.x.org/archive/X11R7.7/doc/man/man1/xdpyinfo.1.xhtml) - Total resolution  

### Installation
```sh
git clone https://github.com/jeffmhubbard/awful
cd awful
sudo install -Dm 755 awful /usr/bin/awful
```

### Configuration
Copy the example config to `~/.config/awful/config`. Edit.  

### Usage
Update image cache:  
```
awful --update PATH
```  
PATH to wallpaper image.  

Lock screen:  
```
awful --lock
```

Capture screen and lock:  
```
awful --capture
```

Additional arguments:  
```
awful -l -- --indicator
```

### Tips
Use `xss-lock`  
```
xset s 600 180 &
xss-lock -l -- awful --lock &
```  
