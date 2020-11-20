
# Steps to Setting up a TLS-Stripping Reverse Proxy
## LightSail
- Create Instance
  - Ubuntu 18, OS Only 
- Manage -> Network  
  - Add Port 443 to firewall
  - Add static ip
- Connect to console
   - sudo adduser username
   - sudo usermod -aG sudo username
   - sudo vi /etc/ssh/sshd_config
      - PasswordAuthentication yes
   - sudo systemctl restart sshd.service

## Putty
- Connect to your virtual machine
- sudo apt update
- sudo apt install npm -y

## CloudFlare
- create an A Record
- SSL Full Strict
- Origin Server Certficate

## Winscp
- Create certificate file
- Create private  file
- Create proxy.js
- Create index.js

## GitHub
- https://github.com/CS3550/ReverseProxySSLStripping 
- copy proxy.js 
- copy index.js

## Putty
- cd example
- npm init -y
- npm i express http-proxy
- which node
- sudo setcap 'cap_net_bind_service=+ep' /usr/bin/node

- tmux 
  - node proxy.js
- tmux 
  - node index.js

Check in browser
