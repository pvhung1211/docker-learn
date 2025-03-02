

```bash
docker container --help

# download image `nginx` from docker hub, start the container and route comming request from host to container 
docker container run --publish 80:80 nginx

# Run in background
docker container run --publish 80:80 --detach nginx

# start: start a stopped one
# run: start a new container 
docker container start <nice_wright>

# List running containers
docker container ls

# List all containers
docker container ls -a

# logging
docker container logs <nice_wright>

# display running process of a container
docker container top <nic_wright>

# display details of one container config
docker container stats <nic_wright>

# performance stats for all containers
docker container inspect <nic_wright>

# start new container interactively
docker container run -it

# run additional command in existing container
docker container exec -it

# remove n container
docker container rm 46d c4 51 
docker container rm 46d -f #force

```


### -it
- -i: Attach container's STDIN [[Interactive Flag]]
- -t: Allocate a [[Pseudo-tty]]
### -ai
- -a: Attach STDOUT/STDERR and forward signals
- -i: Attach container's STDIN

### What happens in  "docker container run"
- Looks for that image locally in image cache, doesn't find anything
- Then looks in remote image repository (defaults Docker Hub)
- Downloads the latest version (by default)
- Create new container based on that image and prepares to start
- Give it a virtual IP on a private network inside docker engine
- Opens up port 80 on host and forwards to port 80 in container

