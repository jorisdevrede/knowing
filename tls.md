# Java

## Truststore
```bash
keytool -importcert -trustcacerts -file /path/to/ca.crt -keystore /path/to/truststore.jks -storepass <secret> -storetype JKS -noprompt
```

## Keystore
```bash
openssl pkcs12 -export \
  -in /path/to/server.crt \
  -inkey /path/to/server.key \
  -CAfile /path/to/ca.crt \
  -name <host> \
  -password file:/path/to/password_file \
  -out keystore.p12
```
