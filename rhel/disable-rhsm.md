# Disable RHSM

```
## Diasble services
systemctl stop rhsm-facts.service && systemctl disable rhsm-facts.service
systemctl stop rhsm.service && systemctl disable rhsm.service
systemctl stop rhnsd.service && systemctl disable rhnsd.service
systemctl stop rhsmcertd.service && systemctl disable rhsmcertd.service

## Disable `subscription-manager` plugins
sed -i 's/enabled=1/enabled=0/g' /etc/yum/pluginconf.d/subscription-manager.conf
sed -i 's/enabled=1/enabled=0/g' /etc/yum/pluginconf.d/product-id.conf
sed -i 's/enabled=1/enabled=0/g' /etc/yum/pluginconf.d/search-disabled-repos.conf

rm -rf /var/lib/rhsm/branded_name /var/lib/rhsm/productid.js /var/lib/rhsm/cache/* /var/lib/rhsm/facts/* /var/lib/rhsm/packages/*
sed -i '/^#/!d' /var/lib/rhsm/repo_server_val/redhat.repo
cat /var/lib/rhsm/repo_server_val/redhat.repo > /etc/yum.repos.d/redhat.repo
rm -rf /etc/rhsm/syspurpose/syspurpose.json /etc/rhsm/facts /etc/yum.repos.d/itaas*
```

