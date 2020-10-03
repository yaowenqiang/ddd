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


# Docker image build

> brew install dive

> dive <conainerId>

# clena up the image

> rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

> docker run --name=src --link=src:ali-src   -it ubuntu /bin/bash


CMD

+ Shell Form  

Commands are expressed the same way as shell commands
Commands get preprended by "/bin/sh -C"
variable expansion etc...

> CMD echo $var1



+ Exec form

JSON array style - ["command" , "arg1"]
Containers don't need a shell
Avoids string muning by the shell
No shell features
    No variable expansion
    No special characters(&&, || >__)


ENTRYPOINT

Can't be overridden at run-time with normal commans - docker run .. <command>
Any command at run-time is used as an argument to ENTRYPOINT



docker daemon log level

+ debug
+ info
+ error
+ fatal

> docker -d -l debug &
> docker -d -l debug  >> <file> 2>&1

> vim /etc/efault/docker/

> DOCKER_OPTS="--log-levle=fatal"
> DOCKER_OPTS="--icc-=false --iptables-=false"

> ip link del docker0
> DOCKER_OPTS="--bip=150.150.0.1/24" #bridge ip
>
> --icc=true  (inter container conmmunication"
> --iptables)


