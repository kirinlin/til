# Postfix on a null client

A null client is a machine that can only send mail. It receives no mail from the network, and it does not deliver any mail locally. A null client typically uses POP, IMAP or NFS for mailbox access.

In this example we assume that the Internet domain name is "example.com" and that the machine is named "hostname.example.com". As usual, the examples show only parameters that are not left at their default settings.

```config
    1 /etc/postfix/main.cf:
    2     myhostname = hostname.example.com
    3     myorigin = $mydomain
    4     relayhost = $mydomain
    5     inet_interfaces = loopback-only
    6     mydestination =
```

Translation:

* Line 2: Set myhostname to hostname.example.com, in case the machine name isn't set to a fully-qualified domain name (use the command "postconf -d myhostname" to find out what the machine name is).

* Line 2: The myhostname value also provides the default value for the mydomain parameter (here, "mydomain = example.com").

* Line 3: Send mail as "user@example.com" (instead of "user@hostname.example.com"), so that nothing ever has a reason to send mail to "user@hostname.example.com".

* Line 4: Forward all mail to the mail server that is responsible for the "example.com" domain. This prevents mail from getting stuck on the null client if it is turned off while some remote destination is unreachable. Specify a real hostname here if your "example.com" domain has no MX record.

* Line 5: Do not accept mail from the network.

* Line 6: Disable local mail delivery. All mail goes to the mail server as specified in line 4.

___
from: http://www.postfix.org/STANDARD_CONFIGURATION_README.html#null_client
