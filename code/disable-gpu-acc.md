# Disable GPU Acceleration

release [October 2019 (version 1.40)#Disable GPU acceleration](https://code.visualstudio.com/updates/v1_40#_disable-gpu-acceleration)

## code --version

```console
1.45.1
5763d909d5f12fe19f215cbfdd29a91c0fa9208a
x64
```

## Result

```shell
~$ cat ~/.vscode/argv.json | sed -e '/\/\//d' | jq .
{
  "disable-color-correct-rendering": true,
  "disable-hardware-acceleration": true
}
```
