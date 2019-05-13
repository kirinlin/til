# Disable GPU Acceleration

issue: [Add a setting to disable gpu acceleration](https://github.com/Microsoft/vscode/issues/15211#)

## code --version

1.33.1

## Add `--disable-gpu`

```
linkirin@m91p: ~$ cat -n /usr/share/applications/code.desktop
     1	[Desktop Entry]
     2	Name=Visual Studio Code
     3	Comment=Code Editing. Redefined.
     4	GenericName=Text Editor
     5	Exec=/usr/share/code/code --disable-gpu --unity-launch %F
     6	Icon=com.visualstudio.code
     7	Type=Application
     8	StartupNotify=false
     9	StartupWMClass=Code
    10	Categories=Utility;TextEditor;Development;IDE;
    11	MimeType=text/plain;inode/directory;
    12	Actions=new-empty-window;
    13	Keywords=vscode;
    14	
    15	[Desktop Action new-empty-window]
    16	Name=New Empty Window
    17	Exec=/usr/share/code/code --disable-gpu --new-window %F
    18	Icon=com.visualstudio.code
```

## Results

```console
linkirin@m91p: ~$ ps -fe | grep code/code | grep gpu
linkirin 19762  7962 14 10:15 ?        00:00:01 /usr/share/code/code --disable-gpu --unity-launch
...
linkirin@m91p: ~$ ps -fe | grep code/code | grep gpu
linkirin 20605     1 24 10:17 ?        00:00:00 /usr/share/code/code --disable-gpu --new-window
```
