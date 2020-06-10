# Turn Off Beep

```console
linkirin@m91p: ~$ lsmod | grep pcspkr
pcspkr                 12718  0 
linkirin@m91p: ~$ sudo rmmod -v pcspkr
linkirin@m91p: ~$ echo "blacklist pcspkr" | sudo tee -a /etc/modprobe.d/blacklist.conf
blacklist pcspkr
```

references:

* [CentOS / Red Hat / Fedora Linux Turn off Beep / Bell Terminal Sound](https://www.cyberciti.biz/faq/rhel-fedora-turn-off-bell-beep-sound/)
* [Howto: Display List of Modules or Device Drivers In the Linux Kernel](https://www.cyberciti.biz/faq/howto-display-list-of-modules-or-device-drivers-in-the-linux-kernel/)
