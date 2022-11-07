# Enable SSH from CLI

Use the `systemsetup` command.

## Check if enabled

`sudo systemsetup -getremotelogin`

## Enable

`sudo systemsetup -setremotelogin on`

ref. link: [How to Enable SSH on a Mac from the Command Line](https://osxdaily.com/2016/08/16/enable-ssh-mac-command-line/)

## Troubleshooting

```shell
linkirin@arale: $ sudo systemsetup -setremotelogin on
setremotelogin: Turning Remote Login on or off requires Full Disk Access privileges.
```

Enables full disk access for `/usr/libexec/sshd-keygen-wrapper`.
