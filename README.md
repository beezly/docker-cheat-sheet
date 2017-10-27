# Docker Cheat Sheet

The idea of this repo is to put together a cheat sheet of commands for quick reference

# Table of Contents
1. [Start a container](#docker-run)
2. [Process Information](#process-information)
3. [Keep it Tidy](#cleanup)

<a name="docker-run"></a>
### Simple run
```
docker run -ti ubuntu bash
```

### Run and attached local directory
```
docker run -ti -v $(pwd):/work ubuntu bash
```

33# Run a specific verison of an OS
```
docker run -ti ubuntu:13.10 bash
```

#33 Map ports 
```
docker run -p 1234:80 nginx 
```

<a name="process-information"></a>
## Process Information

### Shows the currently running containers
```
docker ps
```

### Shows the *existing* containers (remember they don’t disappear when they are not running)
```
docker ps -a
```

<a name="cleanup"></a>
### Delete all "exited" containers
```
docker rm $(docker ps -aq -f status=exited)
```
