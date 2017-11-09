#About this Repo
Docker images for Tribestream 0.9x builds

### Supported tags and respective `Dockerfile` links

* [`0.95` (dockerfiles/0.95/Dockerfile)](https://github.com/tomitribe/tes-0.9x-docker/blob/master/dockerfiles/0.95/Dockerfile)

## How to use this image

### Basic usage
   
    docker run -p 8080:8080 tomitribe/tribestream-0.9x:0.95

### Using mount volumes to deploy an application
    
    docker run -p 8080:8080 -v <AbsolutPathOnDockerHost>:/opt/tribe/tribestream-0.95/webapps/<WarFileName>.war tomitribe/tribestream-0.9x:0.95

### Getting into the container `sh` :
    docker exec -it <yourContainerName> /bin/sh
       
## How to build the image and push it to Tomitribe dockerHub
   **Important:** 
   Remember to copy the `tribestream-0.95.tar.gz`  file inside `dockerfiles/0.95/tarfile` folder before building the docker image.

```
docker login
docker build -t tomitribe/tribestream-0.9x:0.95  -t tomitribe/tribestream-0.9x:latest .
docker push tomitribe/tribestream-0.9x
```    
    
    
    
 
 