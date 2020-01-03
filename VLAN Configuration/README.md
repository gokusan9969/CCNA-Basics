# VLAN (Virtual LAN)

VLANs is used to control broadcast domain.

Advantages of VLANs

-	Broadcast Control – Broadcasts are received by every host on the switched network. In contrast, each VLAN belongs to its own broadcast domain (or IP subnet); thus broadcast traffic from one VLAN will never reach another VLAN.
-	Security – VLANs allow administrators to “logically” separate users and departments.
-	Flexibility and Scalability – VLANs remove the physical boundaries of a network. Users and devices can be added or moved anywhere on the physical network, and yet remain assigned to the same VLAN.

VLAN membership can be configured one of two ways:

-	Statically – Individual switch-ports must be manually assigned to a VLAN.
-	Dynamically – Devices are automatically assigned into a VLAN based on its MAC address. Cisco developed a dynamic VLAN product called the VLAN Membership policy Server (VMPS).

# VTP (VLAN Trunking Protocol)

-	In large switching environments, it can become difficult to maintain a consistent VLAN database across all switches on the network. VTP allows the VLAN database to be easily managed throughout the network.
-	By default, VTP updates are sent out every 300 seconds.

# VTP Modes

Server

–	 Only VTP servers can create, modify or delete entries in the VLAN database. Servers advertise their VLAN database to all other switches on the network. Server can only advertise VLANs 1-1005

Client

–	 VTP clients cannot make modifications to the VLAN database, A client will also forward an update from a server to other clients.

Transparent

–	 VTP transparent switches will not advertise or accept any VLAN database information from other switches (even a server).
