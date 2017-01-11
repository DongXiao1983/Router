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

12. 同步的功能是在互联网早期为了防止路由黑洞和路由环路设计的一个规则（保证AS内防止路由环路，和BGP路由上所有路由器都知道如何将数据包转发到目的地），IGP中的路由必须与BGP中的保持一致，而现在网络IGP已经承载不了BGP的路由条目，所以要关闭   

13. BGP  Summary 
 配置一条指向NULL0的静态路由，ip route prefix mask null0
network network-number [ mask network-mask ] 告诉BGP通告哪些网络，仅当描述网络号出现在IP路由选路中选中后，BGP才会通告它

14.  BGP aggregate
聚合路由在本路由上生成一条聚合路由，吓一跳为 0.0.0.0  

15. BGP Route Policy
Adj-RIBs-In： 从对端路学到的路由，在对端认为是可行的
Local-RIB :
Adj-RIBs-Out:
三步： 1. 计算每条可行路由的优先级， 2. 从所有可用路由中尉特定目的地选出最佳路由，并安装到local-RIB中 ，3. 将相应路由加到Adj-RIBs-Out中向对段宣告

16.   Route Flaps  & Route Dampening 
17. 解决IBGP的水平分割问题，IBGP需要Full Mesh，采用的方法，路由反射和路由联邦

