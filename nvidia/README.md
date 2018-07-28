# nvidia screen brightness config

In order for the screen brightness keys to work on proprietary nvidia-drivers in Xorg environment

# usage

In /usr/share/X11/xorg.conf.d directory
create a file
10-nvidia-brightness.conf
with:
```bash
Section "Device"
    Identifier     "Device0"
    Driver         "nvidia"
    VendorName     "NVIDIA Corporation"
    BoardName      "Quadro K1000M"
    Option         "RegistryDwords" "EnableBrightnessControl=1"
EndSection
```
Reboot
