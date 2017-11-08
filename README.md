# tes-0.9x-docker
Repository to host Docker file(s) to build docker images for the last Tribestream 0.9x build

## Use the image

### Basic usage
   
    docker run -p 8080:8080 tomitribe/tribestream-0.95

### Using mount volumes to deploy an application
    
    docker run -p 8080:8080 -v <AbsolutPathOnDockerHost>:/opt/tribe/tribestream-0.95/webapps/<WarFileName>.war tomitribe/tribestream-0.95

### Getting into container `sh` :
    docker exec -it <yourContainerName> /bin/sh
       
## To build the image and push it to Tomitribe dockerHub
   **Important:** 
   Remember to copy the `tribestream-0.95.tar.gz`  file inside `dockerfiles/0.95/tarfile` folder before building the docker image.

    docker login
    docker build -t tomitribe/tribestream-0.95:latest .
    docker push tomitribe/tribestream-0.95
    
    
    
    
 
 