# kickstart notes

## compare the difference between two kickstart packages

There is no difference. Version: CentOS (Core) 8.2.2004

```old
%packages --instLangs=en
@^Minimal Install
@core
open-vm-tools
```

```new
%packages --instLangs=en
@^minimal-environment
open-vm-tools
```

