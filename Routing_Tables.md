# Routing Tables
<dl>
<dt> Routing Decisions </dt>
<dd> Constains Layer 3 to Layer 2 mappring where routers use ARP Caches to map an IP Address. It makes packet forwarding decisions based on their internal routing tables.

<ht> </ht>

<dt> Routing Tables</dt>
Table kept by the router ot help determine which route entry is the best fir for the network.

<ht> </ht>

A route entry with the **longest prefix** is the most specific network.

<ht></ht>
## Sources of Routing information.
* Directly Connected routers.
  * Learned by physical connection between routers.

*  Static Routes.
  * Manually configured by an admin.
  * Default static route(0.0.0.0/0)is a special case.
      > If I dont't know where, then send out default static route.

* Dynamic Routhing Protocols.
   * Learned by exchanging information between routers.


### Directly Connected Routes
![Directly Connected Routes](https://i.imgur.com/zLCYvwf.png "Directly Connected Route.")

### Static Routes
![](1591139001569.png)
---
### Dynamic routing
![](1591142264926.png)


Based on number of hops (*hop count in RIP*), link bandwidths (OSPF), or other criteria.

### Preventing Loops
#### <u>Split Horizon</u>
Prevents a route learned on one interface from being advertised back out of that same interface.
![](1591142516660.png)

#### <u>Poison Reverse</u>
Causes a route received on one interface to be advertised back out of that same interface with a  metric considered to be infinite.
