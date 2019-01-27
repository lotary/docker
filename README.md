## DockerAndKubernetesExercise
#Redis Image

#simpleweb   

Build image with Dockerfile

simple Node js Webpage image
Dockerfile to build the image with Index.js and package.json

Command to build in docker:

docker build {dockerid}/{imageName} .


#Visits
Using Docker-Compose to build multiple images with network
1. Node js web, will write to redis
2. Redis server 


 docker-compose up --build 

 docker-compose down
 
 docker-compose ps


# React app
1. Install node.js
2. Node -v 
3. npm install -g create -react-app  // using this tool to generate an react-app
4. npm run start -> to start a development server for dev only
5. npm run test -> runs tests associated with the project
6. npm run build -> builds a production version of the application 
7. Dev build : Dockerfile.dev 
    docker build -f dockerfile.dev .
8. docker run -p 3000:3000 bf9ba1744048  <-- the image id it build from the above command
9. docker run -p 3000:3000 -v /app/node_modules -v  $(pwd):/app  <image_id>

10. Or instead using the long docker command each time, 
use the docker-compose.yml + following commands, note - the docker-compose.yml file, with the local file linked to the container and changes are hot deploy to the container. 

docker-compose up
docker-compose down