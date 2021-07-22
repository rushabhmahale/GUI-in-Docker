Video link :-https://drive.google.com/file/d/1r5IOoB0DacfUDt1lrVtLb3qYmuP2_cpg/view?usp=sharing

# GUI-in-Docker
GUi in docker running (Graphical User Interface) in docker 

## Step Should be followed
 1 check docker installed or not systemctl status docker in (Linux) and in windows Run docker version

 2 docker images 

 3 If you dont have any images docker pull centos:latest

 4 Create a container docker run -it --name "CONTAINER" centos:latest
 
 Step inside the Docker 
 - step 1 rpm -q firefox
 - step 2 yum install firefox -y 
 - step 3 firefox (but it failed showing warning no display) 
 
 exit 
 
 5 mkdir dc
 
 ## Create Dockerfile
 
 6 nano Dockerfile
 
 **FROM centos:latest**
 
 **RUN yum install firefox -y**
 
 **CMD ["/usr/bin/firefox"]**
 
 7 docker build -t firefox . ("This will create a image of firefox")
 
 8 docker images ("you will see firefox image")
 
 9 docker container run -it --env="DISPLAY" --net=host firefox 
## images 
- docker pull rushabh21/gui-firefox:v1
