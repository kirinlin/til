# Retrieve `ceph` version

from the CephCluster

```shell
oc get CephCluster/rook-ceph -n rook-ceph -o json | jq -r '.spec.cephVersion.image'
```
