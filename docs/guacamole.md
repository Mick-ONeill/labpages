# Remote Access with Guacomole
[Apache Guacomole](https://guacamole.apache.org/) is an open source remote access solution that allows you to access devices over RDP, VNC, or SSH via the web. 

I installed this to allow me to access the environment if I feel like studying and messing around while at the pub or at work. Plus there's a cool factor. 

## Considerations and recommendations
- Having a public facing site that allows remote access into your environment comes with a lot of security risks.
- Make sure your lab environment is isolated from the rest of your home network.
- Try not to keep any data of consequence on your lab network.  
- Put the Guacamole server behind a reverse proxy such as [NGINX](./nginx.md)
- Configure it with MFA, currently DUO doesn't support Guacamole, so you'll need to use TOTP. 
- Change the password for, and disable, the guacadmin account once you've configured another admin account. 

## Installation
Given the low traffic your instance is likely to handle, you could consider deploying this as an LXC container in Proxmox. 

I mainly used [this script](https://github.com/MysticRyuujin/guac-install) to install it, but there's also some very useful features you can [use here](https://github.com/itiligent/Guacamole-Installer) as well. In my case I used a separate NGINX instance. 

## Gotchas and notes
- I kept running into a lot of problems with Ubuntu 24.04, this was around the install for MYSQL. So I just used Ubuntu 22 LTS instead. 
- It's worth considering installing some of the other features in [Itiligent's](https://github.com/itiligent/Guacamole-Installer) script such as fail2ban which protects against brute force attacks. 


