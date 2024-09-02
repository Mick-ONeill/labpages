# Proxmox

Proxmox is a free to use hyperviser based on linux LVM. It's feature rich and the perfect choice for a home lab. 

You can download it from [www.proxmox.com](https://www.proxmox.com/en/downloads )

## Hardware

Proxmox will run on just about any Intel EMT64 or AMD64 processor with VT/AMD-V respectively. 

I'm justing running a single node with the following specs: 

- AMD Ryzen 9 5900XT CPU (AM4 socket CPUs are going cheap at the moment)
- 64GB RAM
- 2TB nvme SSD. 

If you're not interested in buying a new system and don't have one to repurpose, You can try some of the sites below to get cheap refurbished hardware: 

- [reboot-it.com.au](https://reboot-it.com.au/)
- [www.australiancomputertraders.com.au](https://www.australiancomputertraders.com.au/)

Plus there's ebay, Gumtree, FB market place if you like to live dangerously. 

## Gotchas and notes

- If your graphics uses an NVIDIA GPU you might run into problems with the installer hanging up and crashing. This seems to be a common enough problem. In my case it was resolved by editing the config in GRUB and adding the 'nomodeset' flag. Some useful clues are found on the [support forums](https://forum.proxmox.com/threads/proxmox-8-installer-freezes-at-boot.129341/page-3#post-626839).

- When you login via the GUI, you'll get a message that you don't have a valid subscription. You can ignore this, it's just the tax you have to pay for using it for free. What you will need to do is change the repos Proxmox uses to get updates to the non-subscription version. 

### LXC Containers
For a lot of infrastructure services and other bits an pieces like DNS & DHCP, NGINX, etc.. I strongly recommend using LXC containers with your flavor of supported linux template. LXC containers are not the same as docker containers. They share the linux kernel with Proxmox and are generally lightweight and far more efficient than running a whole VM. 

<img src="/img/wouldyouliketoknowmore.jpg"
        alt="WouldYouLikeToKnowMore"
        width="225"
        height="225"
        style="display: block; margin: 0 auto" />
 
- [linuxcontainers.org](https://linuxcontainers.org/)
- [LXC Vs Docker containters](https://www.docker.com/blog/lxc-vs-docker/)





