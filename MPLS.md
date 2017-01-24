1. Label Switch Routers
   inter-network,  查FIB,
   primarily forwards labeled packets ( swap label) 标签交换
2. Edge LSR
   Lables IP packts ( impose label ) and forwards themm into the MPLS
   Removes labels ( pop label ) and forwards IP packets out of the MPLS domain  
3. control Plane  & Data Plane
   Routing Protocol
   IP Routing table  
   LDP (exchange Lables)
   If receive IPv4 packkages, IP forwarding Tables FIB
   If receive LAB packages, LAB forwarding LFIB  
 4. PHP
 5. Label allocation in a Frame Mode MPLS  Environment
    TDP LDP  : S L I
    BGP : no labels
6. Lable allocation and distribution in a frame mode  MPLS network floolows these steps
  1. IP routing protocols build the IP routing table.
  2. Each LSPR addigns a label to every destination in the IP routing table independently.
  3. LSRs announce their assigned labels to all other LSRs.
  4. Every LSR builds lit LIB, LFIB and FIB data structures based on the received labels.
7. Next-hop LSR
8. FEC  LDP/TDP 形成本地路由表/把本地路由表通告给邻居   LIB/LFB 先查LIB 再查LDP的邻居表  CEF/LFIB  
9. The Procedure to configure MPLS
   0. enable IGP
   1. Configure CEF
   2. Configure MPLS on a frame mode interface
   3. (Optional) Configure the MTU size in label switching
10. Basic MPLS Features
    1. MPLS  is a switching mechanism in which packets are forwarded based on labels
    2. Labels usually correspond to IP destination networks ( qeual to traditional IP forwarding)。
    3. Lables can also correspond to other parameters:
        L3 VPN destination
        L2 circuit
        Outgoing interface on the egress router
        Qos
        Source address
    4.MPLS was designed to support forwarding of non-IP protocols as well

11. MPLS VPN
    Tunnel口用私网地址，建立直连
12. VPN： over Lay VPN  &  Peer-to-Peer VPN (运营商路由器参与)
   L2: X.25 ,  Frame Relay  , ATM
   L3: GRE   IPsec
   
   ACLs, Split Routing, MPLS VPM
13. VRF  for one MPLS VPN
14. 一个VRF在PE端，会生成子路由表，这个自路由表用来传递客户端的私网路由表， PE 创建VRF后 一定要和某个连接CE的路由相连
15. VRF 一台PE创建一个VRF
16. Route Distinguishers
64bit： How will information about the overlapping subnetworks of two customers be propaagated via a single routing protocal?
    Externd the customer addresses to make them unique.
The 64-bit RD is prepended to an IPv4 address to make it globally unqiue.
17. Route Targets
18. MPBGP router  , VPNv4 BGP
19. Community : standerd, no export , local vs, RT
20. A CE router ( customer edge router ) is a router located on the customer premises that provides an Ethernet interface between the customer's LAN and the provider's core network. CE routers, P (provider) routers and PE (provider edge) routers are components in an MPLS (multiprotocol label switching) architecture. Provider routers are located in the core of the provider or carrier's network. Provider edge routers sit at the edge of the network. CE routers connect to PE routers and PE routers connect to other PE routers over P routers
