# KDE Desktop for termux-x11

We got a lot of problems to launch KDE Desktop .So i used 18.04.6 LTS (Bionic Beaver).This version can run KDE easily on vncserver or Termux-x11.

## Phantom Process Killer

We need to Deactive Phantom Process Killer.

[Here](https://github.com/atamshkai/Phantom-Process-Killer/tree/main) 

## Preview

![](https://raw.githubusercontent.com/atamshkai/Ubuntu-18.04-KDE-Desktop-for-termux/main/Screenshot_2023-06-16-20-31-30-533_com.termux.x11.jpg)

# To do

Download it from here.(Use VPN)

https://www.mediafire.com/file/5d8aitew9zjshzr/androkde-fs.tar.xz/file

After downloaded rootfs to Download folder,go to termux and check your shell.

```
echo $SHELL
```

If your shell is bash,

```
echo "killall pulseaudio &>/dev/null" >>~/.bashrc
 
echo "pulseaudio --start --exit-idle-time=-1; pacmd load-module module-native-protocol-tcp auth-ip-acl=127.0.0.1 auth-anonymous=1" >>~/.bashrc
```

If your shell is zsh,

```
echo "killall pulseaudio &>/dev/null" >>~/.zshrc
 
echo "pulseaudio --start --exit-idle-time=-1; pacmd load-module module-native-protocol-tcp auth-ip-acl=127.0.0.1 auth-anonymous=1" >>~/.zshrc
```

```
pkg up -y && pkg i -y x11-repo && pkg i -y proot pulseaudio termux-x11-nightly
```

Close termux

```
exit
```

Then open termux again and go step by step

```
termux-setup-storage
```
```
mv /sdcard/download/androkde-fs.tar.xz ~/
```

Then,

```
tar -xvJf androkde-fs.tar.xz
```

``` 
termux-x11 :1 &
```
Open another session and

```
mv ~/androkde-fs/start-androkde.sh
~/androkde-fs/androkde-binds ~/
```

```
rm -rf ~/androkde-fs/root/.bash_profile
```

```
~/bash ~/start-androkde.sh
```

```
apt update;apt remove -y sudo;apt install -y sudo audacious parole zsh wget pulseaudio

wget https://github.com/atamshkai/Termux-Zsh/raw/main/zsh.tar.xz

tar -xvJf zsh.tar.xz && mv zsh/.* ~/
rm -rf zsh

chsh -s /usr/bin/zsh

```

```
kde
```

## Termux

[Download](https://github.com/termux/termux-app/releases/download/v0.118.0/termux-app_v0.118.0+github-debug_universal.apk)

## Termux-x11

[Download](https://archive.org/download/termux-x11/app-universal-debug.apk)

## Termux-x11 Custom Resolution

1920:1080

