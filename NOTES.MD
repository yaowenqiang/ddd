> /var/lib/docker/containers/{ContainerId}/

hosts
hosts.conf # copied from hosts /var/resolv.conf
> docker run --dns=8.8.8.8  -it --name=dnstest net-image

> docker port <ContainerId>

> apt install brctl
> sudo apt install vim-tiny

> docker run -d -p 5000:80/udp  --name=dnstest net-image
> docker run -d -p 192.168.56.59:5000:80/udp  --name=dnstest net-image
> docker run -d -P  --name=dnstest net-image
