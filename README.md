# cluster4pi
Provide automation to deploy cluster of RPI

## cluster description

The cluster is composed of :

- RPI B+ with 8Gb, called router
- RPI 3 with 32Gb, called node1
- RPI 3 with 16Gb, called node2
- RPI 3 with 32Gb, called node3

Additional supplies are needed :

- An USB hub (4 plugs)
- A power supply 5V 5A. **25 Watt is the minimum, I recommand 50 Watt (10A)**
- A 5 ports network switch


## Network description

The cluster input is the ETH0 of the router board; It expects a DHCP server. 
The router board acces to the switch *via* an USB to Ethernet adapter, ETH1.
The rest of nodes are plugged from ETH0 to switch.

The router provider on ETH1 a DHCP server that work on 10.1.0.0/24 and it acts
as a gateway.