# EIGRP (Enhanced Interior Gateway Routing Protocol)

EIGRP is a Cisco-proprietary Hybrid routing protocol, incorporating features of both Distance-Vector and Link- State routing protocols.
-	EIGRP uses Diffusing update algorithm to determine the best path among all “feasible” paths.
-	EIGRP will form neighbor relationship with adjacent routers in the same Autonomous System (AS)
-	EIGRP uses multicasts on address 224.0.0.10.
-	EIGRP routers do not send periodic, full-table routing updates.
-	EIGRP is a classless protocol and thus supports VLSMs.
-	EIGRP supports IP, IPX, and Appletalk routing.
-	EIGRP Administrative Distance is 90.
-	EIGRP uses Bandwidth and Delay of the Line by default, to calculate its distance metric Reliability, Load and MTU.
-	EIGRP has a maximum hop-count of 224,

# Commands

Router A
-	RouterA(config)# router eigrp as_numbr
-	RouterA(config-router)# network net_addr_neighbour_router
-	RouterA(config-router)# network net_addr_neighbour_router

Router B
-	RouterB(config)# router eigrp as_numbr
-	RouterB(config-router)# network net_addr_neighbour_router
-	RouterB(config-router)# network net_addr_neighbour_router

Router C
-	RouterC(config)# router eigrp as_number
-	RouterC(config-router)# network net_addr_neighbour_router
-	RouterC(config-router)# network net_addr_neighbour_router

# EIGRP Table
-	Neighbor table – list of all neighboring routers. Neighbors must belong to the same AS.
-	Topology table – list of all routes in the AS.
-	Routing table – contains the best route for each known network.
-	EIGRP forms neighbor relationships in the same AS by exchanging Hello packets.
-	Hello packets are sent multicast address 224.0.0.10
-	EIGRP hellos packet are sent every 5 seconds. (high speed wan),slower links are send every 60 seconds
-	Hold timer is three times of Hello timer High speed 15 second, slow link 180 seconds.
