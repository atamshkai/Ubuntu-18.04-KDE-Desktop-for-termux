# KDE Desktop for termux-x11
We got a lot of problems to launch KDE Desktop .So i used 18.04.6 LTS (Bionic Beaver).This version can run KDE easily on vncserver or Termux-x11.

# To do

Download it from here.

https://www.mediafire.com/file/5d8aitew9zjshzr/androkde-fs.tar.xz/file

After downloaded rootfs to Download folder,go to termux and write 

echo "killall pulseaudio &>/dev/null" >>~/.bashrc
 
echo "pulseaudio --start --exit-idle-time=-1; pacmd load-module module-native-protocol-tcp auth-ip-acl=127.0.0.1 auth-anonymous=1" >>~/.bashrc

If your shell is zsh,

echo "killall pulseaudio &>/dev/null" >>~/.zshrc
 
echo "pulseaudio --start --exit-idle-time=-1; pacmd load-module module-native-protocol-tcp auth-ip-acl=127.0.0.1 auth-anonymous=1" >>~/.zshrc

exit

termux-setup-storage

 mv /sdcard/download/androkde-fs.tar.xz ~/
 
pkg up -y && pkg i -y x11-repo && pkg i -y proot pulseaudio termux-x11-nightly

 tar - xvJf androkde-fs.tar.xz
 
termux-x11 :1 &
 
bash ~/start-androkde.sh
 
kde

#Termux-x11

https://github.com/atamshkai/Ubuntu-18.04-KDE-Desktop-for-termux/raw/main/app-arm64-v8a-debug.apk

