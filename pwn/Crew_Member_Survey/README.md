The company is developing an anonymous survey for crew members to fill out on the last day before quota.

They left an alpha version for us to test on the VM! Be sure to only leave good responses!

<br/>

```py
from pwn import * 
p=remote("spaceheroes-crew-member-survey.chals.io", 443, ssl=True, sni="spaceheroes-crew-member-survey.chals.io")
p.interactive()
```

MD5SUM:

```
be1d30648b981fbc1ae8d60625abe667  Borson300VM.bin

6d0abd9a3dada46c4d23c0002d705256  pwnable
```

Author: Marcus Feliciano (A.K.A [B0n3h34d](https://github.com/password987654321))

Solution: Variable overwrite in the custom stack implementation of the VM.
