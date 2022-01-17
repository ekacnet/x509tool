# x509tool
Tools to deal more easily with x509 certificates.

For the moment it's pretty much just one: `x509`.
The tool takes either a certificate as an argument or reads it from stdin.
Output for a certificate looks something like that:

```
CN:            ACCVRAIZ1
SAN:           mail:accv@accv.es
Issuer:        CN=ACCVRAIZ1,OU=PKIACCV,O=ACCV,C=ES
Validity:      valid / 2011-05-05 09:37:37 GMT to 2030-12-31 09:37:37 GMT (8 years to expiration)
Serial:        6828503384748696800
Usage:         Cert signing, CRL signing
Crl:           http://www.accv.es/fileadmin/Archivos/certificados/raizaccv1_der.crl
CA issuers:    http://www.accv.es/fileadmin/Archivos/certificados/raizaccv1.crt
OSCP:          http://ocsp.accv.es
Ciphers:       RSA 4096 / sha1
SKID:          keyid:d287b4e3df37279355f656ea81e536cc8c1e3fbd
AKID:          keyid:d287b4e3df37279355f656ea81e536cc8c1e3fbd
```

If there is multiple certificate (think server certificate + intermediate CA) each certificate will be displayed.

Motivation behind this tool is to have a an easier and more efficient way of showing certificate than using the `openssl x509` command while being a bit more concise.
