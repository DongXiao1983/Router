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

6. IGP  , hello neighbor
   router ad   
   BGP --> 1.create neighbor 2. create network   
   network : interface IGP,   route  BGP

7. BGP neighbor update-source   

8.  EBGP multihop command

9.  build with loopback port. 

BGP: 

10. BGP Syncgronization    
    Rule:   Do not use or advrtise to an external neighbot route learned by IBGP until a matching route has been learned from an IGP. Why ?   
    no Synchronization. / Learned from IGP   

11. BGP Next hop