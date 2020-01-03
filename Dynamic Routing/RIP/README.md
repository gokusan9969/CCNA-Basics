# RIP 

- A standardized Distance Vector protocol, designed for use on smaller networks.
-	RIP sends out periodic routing updates (30 sec)
-	RIP sends out the full routing table every periodic update.
-	RIP uses a form of distance as its metric hop-count 15 (max.)
-	RIP uses the Bellman – ford Distance Vector algorithm to determine the best path to particular destination
-	RIP support only Classful IP routing protocol
-	RIP send updates as broadcasts to address 255.255.255.255
-	RIP v1 not support VLSM
-	RIP support IP and IPX routing
-	RIP routes have an administrative distance of 120

# Commands

Router A
-	Router(config)# router rip
-	Router(config-router)#network net_addr_neighbour_router
-	Router(config-router)#network net_addr_neighbour_router
Router B
-	Router(config)# router rip
-	Router(config-router)# network net_addr_neighbour_router
-	Router(config-router)# network net_addr_neighbour_router


# RIP Version 2 (Routing Information Protocol)

# Commands

Router A
-	Router(config)# router rip
-	Router(config)# version 2
-	Router(config-router)# network net_addr_neighbour_router
-	Router(config-router)# network net_addr_neighbour_router

Router B
-	Router(config)# router rip
-	Router(config)# version 2
-	Router(config-router)# network net_addr_neighbour_router
-	Router(config-router)# network net_addr_neighbour_router


