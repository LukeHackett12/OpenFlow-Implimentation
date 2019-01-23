# Router

![alt text](http://www.quickmeme.com/img/35/35ab5d1edd0d3c429df99f81a4e9fd77a82de9bec59c8a66bfee7f48ec3927a7.jpg)

## How to run

This project is setup with gradle so can be run through the command line so can be run with the following command: 
  ./gradlew clean assemble run

## Connection and Initial exchange

I based the router initial connection off of the specification layed out in the assignment, the initial hello message is 
a single byte that alerts the controller to note its existence and send a feature request. After this the router sends its 
feature information as a Json mapping, currently the included information is : {type, datapath_id, buffers, ports}. The information
currently used is the port and the other fields could be used in the implementation of other codes.

## Client(Destination) connection

The router also has a RESTful API that the clients can send requests to when they want to connect to the network. The client 
can post requests to this API and thi will initiate the addition of a new destination to the network. The router has to make 
the controller aware of the new destination then it can receive the flow table from the controller once it has been generated.

## Forwarding messages

Once the router receives a message from the client through the rest API they will add on the flow table that they have for the
given destination to the packet. This packet is then sent on to the next router in the flow table. Each time the packet is passed 
on the first listing in the flow table is removed and the next one is used as the new destination for the packet. When the router 
encounter a null listing with an ‘isFinal’ flag then the router sends a HTTP post request to the destination where it can be displayed.
