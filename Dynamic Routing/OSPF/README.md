# OSPF (Open Shortest Path First)

OSPF is a standardized Link-State routing protocol, designed to scale efficiently to support larger networks.
-	OSPF allows for a hierarchical network design through the us of Areas
-	OSPF uses the Dijkstra shortest path first algorithm.
-	OSPF is a classless protocol, and thus supports VLSMs.
-	OSPF Traffic is multicast 224.0.0.5 (all OSPF routers) or 224.0.0.6 ( all Designated Routers)
-	OSPF support only IP routing
-	OSPF administrative distance is 110
-	OSPF uses cost as its metric, which is computed based on bandwidth of the link. 
-	OSPF has no hop-count limit.

Router ID Selection
-	Router ID can be manually specified
-	The highest ip address configured on any Loopback interface on the router will become the Router id
-	If no loopback interface exits the highest ip address configured on any physical interface will become the Router ID
-	OSPF Hello packets are sent out on interface every 10 seconds for broadcast  and point-to-point interface and 30 seconds for non-broadcast point to multipoint interface
-	OSPF also has a Dead Interval, which indicates how long a router will wait without hearing any hellos before announcing a neighbor as “down”. Default for Dead Interval is 40 Seconds for broadcast and point-to-point interfaces, and 120 seconds for non-broadcast and point-to-multipoint interfaces.

Neighbor Table
-	Down – indicates that no Hellos have been heard from the neighboring router.
-	Init – indicates a Hello packet has been heard from the neighbor.
-	2-Way – indicates that bidirectional communication has been established.
-	ExStart – indicates that the routers are preparing to share link state information.
-	Exchange – indicates that the routers are exchanging Database Descriptors.
-	Loading – routers are sharing their topology tables with each other.
-	Full – indicates that the routers are fully synchronized.

# Commands

Router A(config)# router ospf 1
Router A(config-router)# network 10.0.0.0 0.255.255.255 area 0
Router A(config-router)# network 20.0.0.0 0.255.255.255 area 0

Router B(config)# router ospf 1
Router B(config-router)# network 20.0.0.0 0.255.255.255 area 0
Router B(config-router)# network 30.0.0.0 0.255.255.255 area 1

Router C(config)# router ospf 1
Router C(config-router)# network 10.0.0.0 0.255.255.255 area 0
Router C(config-router)# network 40.0.0.0 0.255.255.255 area 2

Router D(config)# router ospf 1
Router D(config-router)# network 30.0.0.0 0.255.255.255 area 1
Router E(config)# router ospf 1
Router E(config-router)# network 40.0.0.0 0.255.255.255 area 2


