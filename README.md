# cod4-server-custommaps

Dockerized server for Call of Duty 4 Modern Warfare. Minimizes setup process and server handling to focus on gaming :)

This repo enables your server to run custom maps. For default server and setup guide visit https://github.com/LuisNaldo7/cod4-server .

## Run in Docker

build image

    docker build -t luisnaldo7/cod4-server-custommaps:latest .

execute image

    docker run -d -p 28960:28960 -e SERVER_CONFIG=mp_home_mixed.cfg --network=host --rm --name cod4-server-custommaps-mixed luisnaldo7/cod4-server-custommaps:latest
    docker run -d -p 28961:28960 -e SERVER_CONFIG=mp_home_only.cfg --network=host --rm --name cod4-server-custommaps-only luisnaldo7/cod4-server-custommaps:latest
    docker run -d -p 28962:28960 -e SERVER_CONFIG=mp_home_only_sudden_death.cfg --network=host --rm --name cod4-server-custommaps-only-sudden-death luisnaldo7/cod4-server-custommaps:latest

run container on boot

    docker run -d -p 28960:28960 -e SERVER_CONFIG=mp_home_mixed.cfg --network=host --restart always --name cod4-server-custommaps-mixed luisnaldo7/cod4-server-custommaps:latest
    docker run -d -p 28961:28960 -e SERVER_CONFIG=mp_home_only.cfg --network=host --restart always --name cod4-server-custommaps-only luisnaldo7/cod4-server-custommaps:latest
    docker run -d -p 28962:28960 -e SERVER_CONFIG=mp_home_only_sudden_death.cfg --network=host --restart always --name cod4-server-custommaps-only-sudden-death luisnaldo7/cod4-server-custommaps:latest
