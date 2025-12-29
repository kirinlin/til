# DOS Command - CHCP

`CHCP` - Change Code Page

```console
c:\>ver

Microsoft Windows [版本 10.0.26200.7462]

c:\>where chcp
C:\Windows\System32\chcp.com

c:\>chcp /?
顯示或設定使用中的字碼頁編號。

CHCP [nnn]

  nnn   指定字碼頁編號。

輸入 CHCP (不加參數) 以顯示使用中的字碼頁編號。

c:\>chcp
使用中的字碼頁: 950

c:\>chcp 65001
Active code page: 65001

c:\>help chcp
Displays or sets the active code page number.

CHCP [nnn]

  nnn   Specifies a code page number.

Type CHCP without a parameter to display the active code page number.

```

ref: [Code Page Identifiers](https://learn.microsoft.com/en-us/windows/win32/intl/code-page-identifiers)
