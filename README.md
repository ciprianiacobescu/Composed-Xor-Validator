# Composed-Xor-Validator
A docker compose setup for the XOR validator node with its own polka ui.

# Install Zero tier on node

Create a network in https://my.zerotier.com/

Install the VPN.
https://www.zerotier.com/download/

Join the network you've created. (Read the THREE steps described on the download page)

Check the IP of your node in the central panel ^^. 

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

Add the line `ZeIp=1x.1x.1x.1x` , where 1x.1x.1x.1x is the ip you saw in Zerotier Central.  
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




# Sponsor me 

You can nominate me on XOR at 5FYvE5WvXXKsgMGYZgf1AtFQJPFApcVjakBExzP8ymuLEapF


