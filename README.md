# cod4-server-custommaps

Dockerized server for Call of Duty 4 Modern Warfare. Minimizes setup process and server handling to focus on gaming :)

This repo enables your server to run custom maps. For default server and setup guide visit https://github.com/LuisNaldo7/cod4-server .

## Run in Docker

build image

    docker build -t luisnaldo7/cod4-server-custommaps:latest .

execute image

    docker run -d -p 28960:28960 -e SERVER_CONFIG=<server_config>.cfg --rm --network=host --name cod4-server-custommaps-<server_name> luisnaldo7/cod4-server-custommaps:latest

run container on boot

    docker run -d -p 28960:28960 -e SERVER_CONFIG=<server_config>.cfg --restart always --network=host --name cod4-server-custommaps-<server_name> luisnaldo7/cod4-server-custommaps:latest
