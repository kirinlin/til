---
filename: generate-key-file.md
---

# Generate Key File

ref link: https://theorangeone.net/posts/keepassxc-2.3-migration/#new-key-files

```
dd if=/dev/urandom of=keyfile.key bs=2048 count=1
```

ref link: https://serverfault.com/questions/714410/create-random-file-with-openssl/714412#714412

```
head -c 65535 /dev/zero | openssl enc -aes-256-ctr -pass pass:"$(dd if=/dev/urandom bs=128 count=1 2>/dev/null | base64)" -nosalt  > keyfile.key
```