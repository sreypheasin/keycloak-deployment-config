# deployment-config

## Require 

1. Docker
2. Domain name
3. Cloud Hosting
4. Nginx 

[How to install Nginx](https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-20-04)
[How to install Docker](https://docs.docker.com/desktop/install/windows-install/)

## How to add reverse proxy 

1. Change from root directory to nginx site-available
```bash
cd /etc/nginx/sites-available/
```
2. Create new file to store our proxy config
```bash
touch file-name
```
3. Enable proxy file
```bash
sudo ln -s /etc/nginx/sites-available/file-name /etc/nginx/sites-enabled/
```

## Allow Port ( permit incoming connections )

You can use the command below to configure the Uncomplicated Firewall (UFW) to allow incoming network traffic
```bash
ufw allow [port-number]
```
You can replace [port-number] with your port number. Example: ufw allow 5432

## TLS or HTTPs config 

You can use this comment to add certbot for secure communication 
```bash
sudo certbot --nginx -d example.com
```

THANK YOU
