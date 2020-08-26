# Retrieve pull-secret

```shell
oc get secret/pull-secret -n openshift-config -o json | jq -r '.data.".dockerconfigjson"' | base64 --decode | tee pull-secret.json
```
