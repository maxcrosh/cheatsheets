### Get started with Let's Encrypt
https://letsencrypt.org/

#### Start certbot
docker run -it --rm --name certbot 
  / -v "$PWD/letsencrypt:/etc/letsencrypt" 
  / -v "$PWD/lib/letsencrypt:/var/lib/letsencrypt" certbot/certbot certonly 
  / -m "your.email@email.com" --manual --preferred-challenges dns-01 --no-eff-email 
  / --manual-public-ip-logging-ok --keep-until-expiring --agree-tos 
  / -d domain.com -d www.domain.com --server https://acme-v02.api.letsencrypt.org/directory
