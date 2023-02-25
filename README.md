# .dotfiles-mobile
Dotfiles for my laptop

Install Instructions:

Step 1: Install Arch  
Step 2: Install yay or your preferred AUR tool  
Step 3: Install programs in prerequisites list*  
Step 4: Clone this repository  
Step 5: Copy files into your home directory  

Enjoy!

Prerequisites:
```
yay -S ly sway swaybg alacritty waybar wofi xorg-xwayland xorg-xlsclients glfw-wayland polkit-gnome qt5-wayland qt5ct snapper snap-pac ttf-font-awesome ttf-iosevka ttf-iosevka-nerd ttf-liberation udiskie neovim thunar thunar-volman thunar-archive-plugin sweet-gtk-theme-dark candy-icons-git unzip zathura zathura-pdf-mupdf light gzip gvfs gvfs-mtp bluez bluez-utils blueberry appimagelauncher android-udev imv mpv neofetch wl-clipboard nwg-look wl-mirror
```

*Additional Setup:

Enable display manager:
```
systemctl enable ly.service
```

Enable sudo-less backlight control:
```
usermod -aG video <user>
```

Theming:  
Open nwg-look to configure GTK theme  
Edit the line starting with "output * bg" in ~/.config/sway/config with your preferred wallpaper

Screenshots:  
Create a directory named Pictures in your home folder or edit sway config to change screenshot location 
