# DNS and DHCP
[Dnsmasq](https://help.ubuntu.com/community/Dnsmasq) is a useful local DNS resolver and DHCP server. 

I deployed this as an LXC container using the Ubuntu 22 template. This is where I've set DHCP reservation for the Talos VMs. 

I used [this video](https://www.youtube.com/watch?v=2KYeUCorJ-M) as a crash course introduction on how to configure it. 

## Example of /etc/dnsmasq.conf
```
domain-needed
bogus-priv
no-resolv
server=8.8.8.8
local=/micks.lab/
expand-hosts
domain=micks.lab
dhcp-range=192.160.99.100,192.168.99.200,12h
dhcp-host=BC:24:11:B4:C5:F6,k8-cp-1,192.168.99.20
dhcp-host=BC:24:11:E1:D9:D9,k8-wn-1,192.168.99.25
dhcp-host=BC:24:11:49:07:99,k8-wn-2,192.168.99.26
dhcp-option=option:router,192.168.99.1
dhcp-option=option:dns-server,192.168.99.53
dhcp-option=option:ntp-server,119.18.6.37,162.159.200.1
dhcp-authoritative
```

