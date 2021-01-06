# Troubleshooting vMotion

[Troubleshooting vMotion](https://blogs.vmware.com/vsphere/2019/09/troubleshooting-vmotion.html)
[Understanding and troubleshooting vMotion (1003734)](https://kb.vmware.com/s/article/1003734)

VM=dplog

ssh root@vcsa7.virt.dplab 'grep "relocate" /var/log/vmware/vpxd/vpxd-*.log | grep BEGIN'

opID=kgrn0jic-60240-auto-1ahd-h5:70006249-5c-01

ssh root@dpvmhost12.virt.dplab 'grep kgrn0jic-60240-auto-1ahd-h5:70006249-5c-01 /var/log/hostd.log | grep -i migrate'
ssh root@dpvmhost14.virt.dplab 'grep kgrn0jic-60240-auto-1ahd-h5:70006249-5c-01 /var/log/hostd.log | grep -i migrate'

VMotionDst=6590920832386691275

ssh root@dpvmhost12.virt.dplab 'grep VMotion /var/log/vmkernel* | grep 6590920832386691275'
ssh root@dpvmhost14.virt.dplab 'grep VMotion /var/log/vmkernel* | grep 6590920832386691275'

ssh root@dpvmhost12.virt.dplab 'grep 6590920832386691275 /vmfs/volumes/ESXi-VMFS5-4/dplog/vmware.log'

https://www.controlup.com/iperf-on-esxi/
https://blogs.vmware.com/vsphere/2019/09/how-to-tune-vmotion-for-lower-migration-times.html

