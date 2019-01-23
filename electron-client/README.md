# Client

![alt text](https://cdn.memegenerator.es/imagenes/memes/thumb/24/77/24773268.jpg)

## Build Status
[![Build Status](https://travis-ci.com/LukeHackett12/OpenFlow-Implimentation.svg?branch=master)](https://travis-ci.com/LukeHackett12/OpenFlow-Implimentation)

## How to run

This project is setup with node.js so can be run through the command line so can be run with the following commands: 
    
      $ npm install 
      $ npm start
  
I have also included executables for the project which will be easier to run than installing all the necessary packages.
The client can connect to the network via any router in the network and once in the network it needs to get the network routers
and destinations before it can send a message. Any incoming messages are shown in a pane to the right and will show the sender 
and message content.

## Router Connection

The client is using axios to send a post request to the router with an empty body. The router does not need any extra 
information about the client before sending on the information to the controller so there is no need to send any other 
information. The client also has a page that it can query information from the router from, finding all the routers on 
the network, as well as finding all other destinations in the network. 

## Message Listener

The client uses an express server as a listener in the background that will accept any messages coming in in the known Json 
format and add them to the messages displayed on the screen.
