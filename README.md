# Nginx-Demo

This Demo demonstrates how to set up an NGINX server as a reverse proxy and load balancer for a Node.js application cluster. The setup includes three Node.js applications running on different ports, with NGINX handling SSL termination and HTTP-to-HTTPS redirection.

### Features
- Load balancing across multiple Node.js applications using NGINX.
- SSL termination with a self-signed certificate.
- HTTP-to-HTTPS redirection.
- Serving static files and a simple HTML page.

### Commands used in the Demo-project

##### start nginx
`nginx`

##### get options
`nginx -h`

##### restart nginx
`nginx -s reload`

##### stop nginx
`nginx -s stop`  

##### print logs
`tail -f /usr/local/var/log/nginx/access.log`

##### restart nginx
`nginx -s reload`

##### create folder for nginx certificates
`mkdir ~/nginx-certs`
`cd ~/nginx-certs`

##### create self-signed certificate
`openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout nginx-selfsigned.key -out nginx-selfsigned.crt`