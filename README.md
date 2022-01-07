## Setup Private Docker Registry 

docker-compose up -d

certbot certonly -d registry.sedattanir.xyz --manual --preferred-challenges=dns

sudo su -

# path: /nginx/ssl/
cp /etc/letsencrypt/archive/registry.sedattanir.xyz/* .


cp privkey.pem private.key
cat cert1.pem chain1.pem > certificate.crt