Why using Multicast ?  
1. used when sending same data to multiple receivers  
2. Beeter bandwidth utilization.  
3. Less host/route processing.  
4. Used when addresses of receivers unknown  
5. Used when simulatneous delivery for a group of receivers is required( simulcast )  

Unicast not suitable for creating neighbor.
Broadcast route will sperade the PC's port

-> Multicast advantages
Enhanced efficiency: Controls networks traffic and reduce server and CPU loads  
Optimized performance: Eliminates traffic redundancy  
Distraibuted applications: Makes multipoint applications possible  

-> Multicast Disadvantages  
Mulicast is UDP-based  ( data plane )  
Best-effort delivery: Drops are to be expected.  
No congestion avoidance:  
Duplicates: *   
Out-of-sequence delivery: before UDP add a RTP head.   

Type of Multicast Application:
One to Many : VoIP , VOD   
Many to Many:   
Many to One :  

Multicast Conceptual Model
First-hop
Last-hop(leaf) routers communicate group membership to the network  
Multicast distribution tree  
1. Multicast distrbution:PIM  ， Last-hop: IGMP   
2. 是否转发， 转发机制 ， 转发路径
3. Multicast routing protocols:   IGP:  DVMRP, PIM, MOSPF, CBT
                                  EGP:  MSDP , MSGP  

RPF Checking:
1. forwading Loops
2. 一台路由器收到了一个组播组信源发送的组播流量，当路由器收到了该组播流量，会提取3层包文头源IP，并且在其单播路由表内查找，是否具有去往source的单播路由条目，如果没有，怎该路由器对于该组播组信源没有RPF接口，报文直接在接受口被丢弃，如果该路由器表内拥有去往信源所在网段的单播路由，则查看该路由对应的出接口是否和收到保文的接口是同一个接口，如果是则转发报文，如果不是则丢弃报文。
3. 组播静态路由

PIM
Source-rooted: also called shortest path trees (SPTS)
Rooted at a meeting point in the network: shared trees
   Rendezvous porint (RP)  , core
Dense mode  ---> SPTS
Sparse mode ---> RP

单播： 先有路由条目，再有数据
组播： 先有数据，再建路由条目
RP 人为定义的。

PIM 建立邻居不传路由，运行PIM后路由器接口的工作改变：
1. 对于第一条路由器接收组播流量，如果没有启用PIM，则无论收到什么组播报文都会拆包，丢弃报文
2. 对于最后一跳路由器，连接接收者所在的网段，如果该接口没有启用路由器，则该接口不会周期性发送IGMP query报文
3. 对于中间路由器，彼此互联的物理接口，没有启用PIM，这些路由器不会通过任何接口发送组播

PIM-DM 减裁， route发现下游没有接收组播的接收者（通过IGMP检查是否有组播组成员），在RPF端口反向发送Prune Message。180s,计时器，时间段内不再发送。
       每三分钟一次的修剪和泛洪。

所有启用PIM的接口，把流量放下去。

PIM-SM
Support both source and shard trees , Pull mode.
