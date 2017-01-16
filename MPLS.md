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
