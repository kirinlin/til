# cryptsetup Tips

see: https://github.com/rhinstaller/kickstart-tests/blob/master/autopart-luks-1.ks.in

```
# Try to use the passphrase.
echo "passphrase" | cryptsetup luksOpen --test-passphrase "${crypted}"
```
