# Composed-Xor-Validator
A docker compose setup for the XOR validator node with its own polka ui.

It is assumed you already installed: docker, docker-compose, git, nano packages. 

# Install Zero tier on node

Create a network in https://my.zerotier.com/

![Zcreation](/images/zetorier_network_creation.png "Zcreation")

We'll assume you have chose the 10.147.17.* 

Install the VPN.
https://www.zerotier.com/download/

Join the network you've created. (Read the THREE steps described on the download page)

Aprove the node as a member from Zerotier Central.

Change the IP of your XOR node in the central panel to 10.147.17.101. 

![Zedit](/images/zetorier_network_creation2.png "Zedit")

## Install Zerotier on your PC 

Install Zerotier on your PC and ping the node's IP.


# Prepare your project data

Run in terminal
`git clone https://github.com/ciprianiacobescu/Composed-Xor-Validator.git`

Then 

`cd Composed-Xor-Validator`

`mkdir -m777 -v chain`

`sudo chown -R 10000:10000 ./chain`


## Create a .env file

`nano .env`

Add the line `ZeIp=10.147.17.101` , where 10.147.17.101 is the ip you saw in Zerotier Central.  
Add the line `XOR_NODE_NAME=YourXORnamu` 

## Pulling the images

Terminal:
`docker-compose pull`

## Check to see if configs are ok

Terminal:
``docker-compose config``

## Starting the beast

Terminal: ``docker-compose up -d``

## Stoping the beast

Terminal: ``docker-compose stop``

## Log binging

Terminal: ``docker-compose logs -f``


# Use the UI to see the beast!

http://10.147.17.101:28080

## Set the custom endpoint 
![CustomEndpoint](/images/xor_node_custom_endpoint.png "CustomEndpoint")

## Rotate key using UI

Xor key roation si very simple with the polkaui.

![RotateKeys](/images/xor_rpc_rotate_keys.png "RotateKeys")

# Next ...

Wait for the node to sync and then finish the Validator configuration

# Sponsor me 

You can nominate me on XOR at `5FYvE5WvXXKsgMGYZgf1AtFQJPFApcVjakBExzP8ymuLEapF`



