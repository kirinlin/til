# Hide Version

reference link: [How to Hide Apache Version Number and Other Sensitive Info](https://www.tecmint.com/hide-apache-web-server-version-information/)

```shell
egrep '^Server(Signature|Tokens)' /etc/apache2/conf-available/security.conf
sudo sed -i 's/^ServerTokens .*/ServerTokens Prod/' /etc/apache2/conf-available/security.conf
sudo sed -i 's/^#ServerSignature Off/ServerSignature Off/' /etc/apache2/conf-available/security.conf
sudo sed -i 's/^ServerSignature On/#ServerSignature On/' /etc/apache2/conf-available/security.conf
egrep '^Server(Signature|Tokens)' /etc/apache2/conf-available/security.conf
```
