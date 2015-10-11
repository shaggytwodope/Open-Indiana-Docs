# Example of modifying boot menu on OpenIndiana

adrian@openindiana-hipster:~$ bootadm list-menu # list current boot menu(roughly, and location of it)
the location for the active GRUB menu is: /rpool/boot/grub/menu.lst
default 2
timeout 30
0 OI hipster
adrian@openindiana-hipster:~$ sudo nano /rpool/boot/grub/menu.ls # edit the boot menu accordingly and save
adrian@openindiana-hipster:~$ sudo bootadm update-archive #and you're done, boot menu update!