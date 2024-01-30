# .dotfiles-mobile
Dotfiles for my laptop

Install Instructions:

Step 1: Install Arch  
Step 2: Install yay or your preferred AUR tool  
Step 3: Install programs in prerequisites list*  
Step 4: Clone this repository  
Step 5: Copy files into your home directory  

Enjoy!

Speed up build times:
```
#/etc/makepkg.conf

MAKEFLAGS="-j$(nproc)"
```

Prerequisites:
```
yay -S ly sway swaybg swayidle swaylock alacritty waybar wofi xorg-xwayland xorg-xlsclients glfw-wayland polkit-gnome qt5-wayland qt5ct snapper snap-pac ttf-font-awesome ttf-iosevka ttf-iosevka-nerd ttf-liberation udiskie neovim thunar thunar-volman thunar-archive-plugin unzip zathura zathura-pdf-mupdf gzip gvfs gvfs-mtp bluez bluez-utils blueberry appimagelauncher android-udev imv mpv neofetch wl-clipboard wl-mirror gnome-bluetooth-3.0 cups cups-pdf catppuccin-gtk-theme-mocha exfat-utils file-roller grim grimshot htop lldb llvm mako man-db nodejs npm python python-pip tree-sitter-cli system-config-printer grub-btrfs inotify-tools
```

Laptop specific prerequisites:
```
yay -S light tlp
```

Nice apps:
```
yay -S gimp discord github-cli gnome-disk-utility google-chrome libreoffice-fresh steam onedriver
```

*Additional Setup:

Enable important services:
```
systemctl enable ly.service
systemctl enable bluetooth.service
systemctl enable cups.socket
systemctl enable tlp.service
systemctl mask systemd-rfkill.service
systemctl mask systemd-rfkill.socket
systemctl enable grub-btrfsd
```

Enable sudo-less backlight control:
```
usermod -aG video <user>
```

Setup snapper:
```
umount /.snapshots
rm -r /.snapshots
snapper -c root create-config /
```

Theming:  
Use gsettings to set the GTK theme.
Edit the line starting with "output * bg" in ~/.config/sway/config with your preferred wallpaper.

Screenshots:  
Create a directory named Pictures in your home folder or edit sway config to change screenshot location. 
