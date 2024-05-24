# GPG reports error under WSL

Got some errors under WSL2 (Windows Subsystem for Linux) like:

```shell
gpg: signing failed: Inappropriate ioctl for device
gpg: [stdin]: clear-sign failed: Inappropriate ioctl for device
```

There is no prompt for passphrase. Add `export GPG_TTY=$(tty)` then you will be fine.