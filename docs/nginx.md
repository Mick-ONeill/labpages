# Nginx Reverse proxy
[NGINX](https://nginx.org/en/) is a popular opensource webserver and proxy. It is commonly used as a [reverse proxy](https://www.f5.com/glossary/reverse-proxy), and is very useful in a home lab if you want to host multiple sites over standard ports on the same IP and / or add an extra layer of security. Another useful advantage is letting NGINX handle all of the SSL handoff, so that way you're only maintaining SSL certificated in the one place. 

For SSL certificates, I'm using Let's Encrypt as it's both free and can be setup to automatically renew certificated. However, this does come with some caveats which will be detailed in the **Gotchas and Notes** section of this page. 

To Setup NGINX and Let's Encrypt I followed [this guide](https://gist.github.com/gmolveau/5e5b0bd2773100d85d9302d0fa96632d). If you want to put NGINX in front of Guacamole (Strongly recommended) be sure to [RTFM!](https://guacamole.apache.org/doc/gug/reverse-proxy.html#nginx).

## Gotchas and Notes
- The example configuration in gmolveau's guide includes configuration that certbot (Let's Encrypt) automatically generates. Just remove any of the config that has the ```# managed by certbot``` note at the end of the line. 
- For certbot to work you must have all of your external DNS and networking setup. Certbot verifies your domain by querying itself on that domain. Your firewall / router will need to port-forward and allow both port 80 and 443, and can't be geo-fenced (ask me how I know) for certbot to work correctly. 
- The site config might look a dogs breakfast after you enable certbot with NGINX, unless you know what you're doing, don't mess with it. I tried, I failed, I have no idea what I'm doing. 