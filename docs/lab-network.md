# Lab Network
As mentioned in the [Guacamole page](./guacamole.md), it is highly recommended to keep your lab network isolated from the rest of your home network. I've done this via VLANs and a firewall. 

For this I strongly recommend a switch that has layer 2 management capability and a firewall and / or home router that supports the following features:  

- 802.1q
- Port forwarding
- Dynamic DNS (nice to have)
- ACLs / firewall policies, and NAT rules. 
- What ever protocol your ISP uses auth such as PPPoE

Some cheap and cheerful options for either are:  

- Ubiquity switches and routers such as [Edge Switch](https://www.ubnt.com.au/edgeswitch-5-xp), and [Edge Router](https://www.ubnt.com.au/?rf=kw%3Fkw%3Dedge%2520switch%26rf%3Dkw&sortby=lowest_price)  
- [TP-Link](https://www.amazon.com.au/TP-Link-5-Port-Gigabit-Ethernet-TL-SG105E/dp/B00K4DS5KU/ref=pd_bxgy_thbs_d_sccl_1/358-8886976-7198360?pd_rd_w=9DlBb&content-id=amzn1.sym.fe5a09f1-8566-41f4-bd47-fa1ed34fa9f8&pf_rd_p=fe5a09f1-8566-41f4-bd47-fa1ed34fa9f8&pf_rd_r=BJJ5JME2VXT6CJF5TWS0&pd_rd_wg=G2p4s&pd_rd_r=b377e97e-e506-4f86-bf0c-6d7ddeced3c5&pd_rd_i=B00N0OHEMA&th=1) Have suitable small switches.  
- For the more adventureous you could get a [small fanless pc like this](https://www.amazon.com.au/Firewall-Appliance-OPNsense-Untangle-HUNSN/dp/B0BJQ3KHRS/ref=sr_1_62?crid=17J7YRUEQNK03&dib=eyJ2IjoiMSJ9.3VNFgQoIV_0vai-U80AhTOcji88YVNi7PymQvyW5dKr1Q6ZpiEwAGPgFplps_W35sP0YGVW0fnmU-D4dN55gNjw7XtANLFHh_l-mOg6rVX86K2xWw9jdoR_3mIxjBrYjrtRFRjpR9B_By2KRzAO5Zha69wJCJ1I2Xk8viUh9oDgHGhG4PtayRUE9JWO5J7xdNgmZt9l8gLr6ianY9BC9TXDTnXGdv8M3GbYW_4DWECoyXWiLCUkvAXvGtZiTMU68EtumJh3_7cmkwF61CNeD1Ma2gjgnbW_Ez8ZfSseBMQ0.OAlbiA1e5M5m7EbsTLK7ftW4ZAF8APJJ2_VaJFGI-BQ&dib_tag=se&keywords=linux%2Bfanless%2Bmicro%2Bpc&qid=1725243081&sprefix=linux%2Bfanless%2Bmicro%2B%2Caps%2C281&sr=8-62&th=1) and install [Community PFSense](https://www.pfsense.org/download/). 