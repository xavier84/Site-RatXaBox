+++
title = "Couchpotato"
date =  2017-11-26T09:17:16+01:00
weight = 5
+++



## Installation de Let's Encrypt sur le script ratxabox

```
service nginx stop
cd /tmp
wget https://dl.eff.org/certbot-auto
chmod a+x ./certbot-auto
```

change par ton domain
```
./certbot-auto certonly        \
  --standalone                 \
  --rsa-key-size 4096          \
  --agree-tos                  \
  --email john.doe@mondedie.fr \
  --domains mondedie.fr        \
  --domains www.mondedie.fr
  ```

  tu modifi dans

```
ssl_certificate /etc/letsencrypt/live/www.votresite.fr/fullchain.pem;
ssl_certificate_key /etc/letsencrypt/live/www.votresite.fr/privkey.pem;

```
et un start
```
service nginx start
```