# RPI Home Network Appliance
I currently run a RPi connected to ISP router via ethernet for a number of network services. All of which have been installed and configured (aka hacked together) by hand over the years so I've decide to pull the setup and config into maintainable repo will scripts to auto deploy.

Services that run on the RPi are:

* DHCP service and Internal DNS using [dnsmasq](https://wiki.debian.org/dnsmasq)
* External Encrypted DNS via Cloudflare using [Argo](https://blog.cloudflare.com/argo-tunnels-that-live-forever/) and [cloudflared](https://github.com/cloudflare/cloudflared)
* Web proxy used occassionally for testing using [SQUID](http://www.squid-cache.org/)
* [Homebridge](https://homebridge.io/) for hacking together various Apple Homekit integrations

Services to add:

* Syslog server
* VPN server using [Wireguard](https://www.wireguard.com/)

# Setup

Plan is to write some quick and dirty ansible scripts to configure the base image on the RPi. Plan is to run services containerised where possible. Going to look to use [Harbourmaster](https://gitlab.com/stavros/harbormaster) to orchestrate the deployment of containers.

All config will set within this repo. 

Need to consider secret management. 
