# Retrieve `root-ceph` version

```shell
oc get deployment/rook-ceph-operator -n rook-ceph -o json | jq -r '.spec.template.spec.containers[0].image'
```


