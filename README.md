# Linux Grub

This repository stores some information about using grub in Linux!

## Probing for Other OS

**Ubuntu**  
```bash
sudo update-grub2
```

**Arch**  
```bash
# Install os-prober
sudo pacman -S os-prober nvim
# Open the GRUB configuration file
sudo nvim /etc/default/grub
```

Look for the line that starts with:  
```bash
# Change from true to false or add this new line
GRUB_DISABLE_OS_PROBER=false
```

Regenerate the GRUB Configuration:  
```bash
sudo grub-mkconfig -o /boot/grub/grub.cfg
# Found Windows 10 on /dev/sda1
# Found Ubuntu 20.04 on /dev/sda2
```
