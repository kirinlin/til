# pinentry via SSH

reference: [Enter passphrase with pinentry in Terminal via SSH connection](https://gpgtools.tenderapp.com/kb/faq/enter-passphrase-with-pinentry-in-terminal-via-ssh-connection)

```shell
export GPG_TTY=$(tty)
if [[ -n "$SSH_CONNECTION" ]] ;then
    export PINENTRY_USER_DATA="USE_CURSES=1"
fi
```
