1. BGP Characteristics
   Periocdic keepalibe messages to verify TCP connectivity.
   IGP --> "Hello package": open & keepalive
   Rich metrcs (attributes ), the metrics is only one of the attributes.

2. BGP Databases
   Neighbor table
   BGP table ( forwarding database )  --- no redundency 
   IP routing table 

3. BGP Message Types
   Open
   Keepalive
   Update --> transport route
   Notification  --> When error happened

4. EBGP IBGP
   BGP peer :: BGP neigbor
   BGP speakers :: BGP router
   EBGP : directly connected between AS
   IBGP : the neighbors do not have to be directly connected.
   IGP : has the multicast address
   BGP : no multicast address

5. How to resolved the router black hole
   a. physical connection full mesh
   b. BGP neighbor full mesh
   c. BGP -> IGP ( LAB )
   d. MPLS 
    
   
