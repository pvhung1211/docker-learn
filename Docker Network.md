
#### Defaults
- Each container connected to a private virtual network "[[Bridge]]"
- Each virtual network routes through [[NAT]] [[Firewall]] on host IP
- All containers on a virtual network can talk to each other without -p
- Best practice is to create a new virtual network for each app
	- network "my_web_app" for mysql and php/apache containers
	- network "my_api" for mongo and nodejs containers

#### Batteries included
- Make a new virtual network
- Attach containers to more than one virtual network (or none) 
- Skip virtual networks and use host IP (--net=host)
- Use different Docker network drivers to gain new abilities
