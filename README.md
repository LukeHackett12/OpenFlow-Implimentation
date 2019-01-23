# OpenFlow Implimentation

![alt text](https://www.researchgate.net/profile/Chanthan_Hel/publication/268813246/figure/download/fig1/AS:295364365176832@1447431760135/ICN-over-SDN-OpenFlow-architecture-for-one-autonomous-system.png)

## Introduction
In this assignment I have implemented a partial implementation of the OpenFlow communication protocol. In this implementation it is assumed that the Controller for this network is running when the routers try to connect. Routers have a hard coded address for the Controller that they will use to initiate the connection process, which involves making the controller aware of its presence and sending the features that it has to the controller. For this implementation there is not much done with the features however this makes room for future expansions or addition of other openflow codes. 
I have made a client to demonstrate some of the capabilities of this network. It will connect to the network via an IP of a Router. Once this happens it can send messages to any destinations on the network starting at any router on the network.

## Overall thoughts on the Project
The network is a proof of concept for an Openflow implementation. The flow tables are in place and the router functionality is barebones but functional. The client is a good way of seeing a practical application for how a network can be used and makes it easier to see how the network works. Overall I would have liked to have had time to implement distance vector routing in the project but it was not possible unfortunately.
