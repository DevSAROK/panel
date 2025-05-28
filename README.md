# panel
Pufferpanel installation codes-

$ apt update\n
$ apt upgrade -y\n
$ mkdir -p /var/lib/pufferpanel\n
$ docker volume create pufferpanel-config\n
$ docker create --name pufferpanel -p 8080:8080 -p 5657:5657 -v pufferpanel-config:/etc/pufferpanel -v /var/lib/pufferpanel:/var/lib/pufferpanel -v /var/run/docker.sock:/var/run/docker.sock --restart=on-failure pufferpanel/pufferpanel:latest\n
$ docker start pufferpanel\n
$ docker exec -it pufferpanel /pufferpanel/pufferpanel user add
