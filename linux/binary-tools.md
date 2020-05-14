# binary tools

## ldd - print shared object dependencies

link: http://man7.org/linux/man-pages/man1/ldd.1.html

```
~$ ldd /usr/bin/ipmitool
	linux-vdso.so.1 =>  (0x00007ffc5c3df000)
	libm.so.6 => /lib/x86_64-linux-gnu/libm.so.6 (0x00007f362bc87000)
	libreadline.so.6 => /lib/x86_64-linux-gnu/libreadline.so.6 (0x00007f362ba41000)
	libcrypto.so.1.0.0 => /lib/x86_64-linux-gnu/libcrypto.so.1.0.0 (0x00007f362b664000)
	libc.so.6 => /lib/x86_64-linux-gnu/libc.so.6 (0x00007f362b29b000)
	libtinfo.so.5 => /lib/x86_64-linux-gnu/libtinfo.so.5 (0x00007f362b072000)
	libdl.so.2 => /lib/x86_64-linux-gnu/libdl.so.2 (0x00007f362ae6d000)
	/lib64/ld-linux-x86-64.so.2 (0x0000555e440af000)
```

## readelf - display information about ELF files

link: http://man7.org/linux/man-pages/man1/readelf.1.html

```
~$ readelf -d /usr/bin/ipmitool | grep 'NEEDED'
 0x0000000000000001 (NEEDED)             Shared library: [libm.so.6]
 0x0000000000000001 (NEEDED)             Shared library: [libreadline.so.6]
 0x0000000000000001 (NEEDED)             Shared library: [libcrypto.so.1.0.0]
 0x0000000000000001 (NEEDED)             Shared library: [libc.so.6]
```