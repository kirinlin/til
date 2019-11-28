# Get interfaces name and its MAC address

Tested under: RHEL7.7, Ubuntu 14.04, Ubuntu 16.04, Ubuntu 18.04

```
inets="$( sudo ls -1 /sys/class/net | egrep ^\(eth\|en\) )"; \
for inet in ${inets}; do echo "${inet} - $( sudo cat /sys/class/net/${inet}/address )"; done
```
