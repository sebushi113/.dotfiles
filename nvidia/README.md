# nvidia screen brightness config

In order for the screen brightness keys to work on proprietary nvidia-drivers in Xorg environment

# usage

go to  
/usr/share/X11/xorg.conf.d    
create a file  
10-nvidia-brightness.conf  
with:
```bash
Section "Device"
    Identifier     "Device0"
    Driver         "nvidia"
    VendorName     "NVIDIA Corporation"
    BoardName      "QGeForce GT 425M"
    Option         "RegistryDwords" "EnableBrightnessControl=1"
EndSection
```
Reboot
