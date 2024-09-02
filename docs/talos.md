# Kubernetes on Talos linux

Talos is a very lightweight linux distribution centered around Kubernetes. It more or less allows you to stand up a K8s cluster out of the box (with some caveats). 

They have a very useful [guide for getting start on Proxmox](https://www.talos.dev/v1.7/talos-guides/install/virtualized-platforms/proxmox/). 

## Gotchas and notes
- The best way to configure networking for your nodes is via DHCP assignment / reservation, it is best to do this after you create the VM (so you can get the MAC address) but before you turn any of them on. See the [page on dnsmasq ](./dnsmasq.md) for more information. 
- Setup your control plane node first, just note that you'll need to complete the steps in the [Using the Cluster](https://www.talos.dev/v1.7/talos-guides/install/virtualized-platforms/proxmox/#using-the-cluster) section first before everything comes up healthy in the console for the node. Once you're control plane node is all green setting up the worker nodes is a breeze. 
- Talos does not use kubeproxy, and does not provide a load balancer. I installed [metallb](https://metallb.universe.tf/installation/) to use as a load balancer. 
- [Helm](https://helm.sh/docs/) is also useful for installing and deploying various things into your cluster. 