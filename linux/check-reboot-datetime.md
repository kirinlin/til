# Check reboot datetime

command: `sudo last | grep reboot | head -n 3`

## Ubuntu 18.04

```console
~$ sudo last | grep reboot
reboot   system boot  4.15.0-109-gener Thu Jul  9 13:07   still running
reboot   system boot  4.15.0-109-gener Thu Jul  9 13:03 - 13:07  (00:03)
reboot   system boot  4.15.0-109-gener Thu Jul  9 13:00 - 13:03  (00:02)
```

## RHEL 7.7

```console
~$ sudo last | grep reboot | head -n 3
reboot   system boot  3.10.0-1062.18.1 Thu Jul 16 10:48 - 11:05  (00:16)    
reboot   system boot  3.10.0-1062.18.1 Wed Jul 15 09:37 - 11:05 (1+01:28)   
reboot   system boot  3.10.0-1062.18.1 Tue Jul  7 09:42 - 11:05 (9+01:23)   
```
