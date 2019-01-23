# Controller

## How to run

This project is setup with gradle so can be run through the command line so can be run with the following command: 
  ./gradlew clean assemble run 
The controller is responsible for generating flow tables and keeping an updated list of the routers and destinations that 
have made themselves known in the network. 

## Flow Tables

The flow tables generated in this are per destination and as a proof of concept the message 
is forwarded to each router in the network before finally being dispatched to the final destination. 
On the connection of a new destination the flow tables are updated and dispatched to each of the routers with 
flows for each destination starting at its own address.

## Other router interactions

The Controller has a list of codes that it can interpret from the router. These codes are the feature response and the 
router hello. The hello message is what prompts the controller to send a feature request to the router and once it 
receives the feature response it can store this information with the router in a list of all routers currently connected.
