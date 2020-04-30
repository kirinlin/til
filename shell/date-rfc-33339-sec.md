# date RFC-3339 sec

## Linux

```
date --rfc-3339=seconds
```

## macOS

```
/bin/date "+%Y-%m-%d %H:%M:%S%z"
```

### --rfc-3339=date

```
/bin/date "+%Y-%m-%d"
```

### --rfc-3339=ns

Doesn't support nanoseconds.