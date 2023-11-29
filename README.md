## Docker
docker is a tool designed to make it easier to create deploy and run applications by using containers.


## To install docker in linux

sudo yum install docker -y

## to start the docker
sudo systemctl start docker
## to check docker is installe or not
docker --version

## to login to dockerhub account
docker login
give the login credentials and password

## to list of images
docker images

## to build a images from a dockerfile
 docker build -t name (t indicates the tag)

 ## to pull the image from the docker hub:

 docker pull imagename

 ## to run the container out of the image
 docker run -it --name name of the container -p port number image name
 
 example imagename is nginx and container name is c1 need to run on specific port 8000
 
 docker run -it --name c1 -p 8000:8000 nginx (-it indicates run in a interactive mode)
 you can use -d for detached mode.

 ## to check the list of running containers
 docker ps
 ## to check the list of all the containers.
 docker ps -a

 ## to remove the images
 docker rmi imagename
 ## to remove the container
 docker rm containername / id
 ## to stop the running container
 docker stop containername/id

## Dockerfile essential commands
  FROM
  ENV
  RUN
  ENTRYPOINT
  ADD
  WORKDIR
  EXPOSE
  USER 
  VOLUME

  # to push the image to your own dockerhub account
  first you need to tag the image
  
  docker tag name orginalimage name
  
  for ex  i need to make ubuntu offical in my own name you can tag by giving your name
  
  docker tag ubuntu balaubuntu
  
  after the tag the image is created on your own name
  
  to push
  
  docker push balaubuntu.

  # to get a image from the running container.
  docker commit conatinername newimagename
  ex: conatiner is c8 and image is nginx:v2
  docker commit c8 nginx:v2

