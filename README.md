# Debian-Prince

This is Debian Bookworm Xfce4 Desktop.

For Android 12 & 13,before you install it,

Disable phantom process killer. 

[Here](https://github.com/atamshkai/Phantom-Process-Killer/tree/main) 
# Preivew

![](https://raw.githubusercontent.com/atamshkai/Debian-Prince/main/debian-prince.png)

# To Do

### Install zsh & some packges 

#### You can skip these steps if you've already install them
``` 
pkg up -y && pkg i -y x11-repo proot-distro pulseaudio zsh wget termux-x11-nightly
```
```
wget https://github.com/atamshkai/Termux-Zsh/raw/main/zsh.tar.xz
```
```
tar -xvJf zsh.tar.xz
```
```
chsh -s zsh 
```

### For Sound, 
``` 
echo "killall pulseaudio &>/dev/null" >>~/.zshrc 
``` 
```
echo "pulseaudio --start --exit-idle-time=-1; pacmd load-module module-native-protocol-tcp auth-ip-acl=127.0.0.1 auth-anonymous=1" >>~/.zshrc 
```

### Give Storage Permission
``` 
termux-setup-storage 
```

### Install Debian Proot-Distro
```
proot-distro install debian
```

### Login To Debian Distro
```
proot-distro login debian --shared-tmp
```

### Install Needed Packages
```
apt-get update;apt-get full-upgrade -y
```
```
apt install -y apt-utils dialog nano wget
```
```
apt install -y zsh xfce4 xfce4-terminal chromium firefox-esr parole audacious pulseaudio alsa-utils telegram-desktop
```

### Change Shell
```
chsh -s /usr/bin/zsh
```

### Download Prince's Desktop[Usa Vpn]
```
cd $HOME;wget https://archive.org/download/debain-prince/prince.tar.xz
```

### Unzip File
```
tar -xvJf ~/prince.tar.xz
```

### Move Zip File To Download
```
mv ~/prince.tar.xz /sdcard/download
```

### Link To Phone Storage
```
ln -s /sdcard ~/sdcard
```

### Restart Distro
```
exit
```

### Restart Termux
```
exit
```

### Open Termux Again & Start Termux-X11
```
termux-x11 :0 &
```

### Login To Debian Proot-Distro
```
proot-distro login debian --shared-tmp
```

### Add additional commands To Bin
```
echo "export PULSE_SERVER=127.0.0.1;env DISPLAY=:0 dbus-launch --exit-with-session xfce4-session &>/dev/null" >>/usr/local/bin/xfce
```
```
echo "xfce &>/dev/null" >>/usr/local/bin/prince
```

### Give Permission To Commands
```
chmod +x /usr/local/bin/*
```

### Start Debian Prince Desktop
```
prince
```

### Stop Desktop
```
pkill -f com.termux.x11
```

### Termux 
[Download](https://github.com/termux/termux-app/releases/download/v0.118.0/termux-app_v0.118.0+github-debug_universal.apk) 

### Termux-x11 
[Download](https://github.com/termux/termux-x11/releases) 

## Termux-x11 Custom Resolution
1920:1080

[Contact me](https://t.me/atamshkai) 
