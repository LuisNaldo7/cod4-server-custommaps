# cod4-server-custommaps


## Run in Docker

Add game files (directories /main & /zone) to repository root dir.

build image

    docker build -t luisnaldo7/cod4-server-custommaps:latest .

execute image

    docker run -d -p 28960:28960 --rm --network=host --name cod4-server-custommaps luisnaldo7/cod4-server-custommaps:latest

run container on boot

    docker run -d -p 28960:28960 --restart always --network=host --name cod4-server-custommaps luisnaldo7/cod4-server-custommaps:latest
