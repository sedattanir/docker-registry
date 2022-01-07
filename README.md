## Setup Private Docker Registry 

```
certbot certonly -d registry.sedattanir.xyz --manual --preferred-challenges=dns

sudo su -`

# path: /nginx/ssl/

cp /etc/letsencrypt/archive/registry.sedattanir.xyz/* .
cp privkey.pem private.key
cat cert1.pem chain1.pem > certificate.crt
docker-compose up -d
```
