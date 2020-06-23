## docker-pipeline
docker-pipeline steps by steps

docker run -d -u root --name jenkins -p 8080:8080 -p 50000:50000 -v /root/jenkins_2112:/var/jenkins_home jenkins/jenkins

## Get password
docker exec -it jenkins cat /var/jenkins_home/secrets/initialAdminPassword

# Plugins
1. CloudBees Docker Build and Publish plugin
2. Docker

# Add DockerHub Credentials

### Manage Jenkins > Configure System > Manage Credentials



## Docker image creation

# Dockerizing a Node.js web app
https://nodejs.org/en/docs/guides/nodejs-docker-webapp/

# Using Docker with Pipeline
https://www.jenkins.io/doc/book/pipeline/docker/


docker images

docker run -p 49160:8080 -d 0c26709d740b

## Create Pipeline

Name: Docker-Pipeline
#### "Pipeline" option
#### Pipeline > Pipeline script from SCM
#### SCM > Git
#### Repository Url > github...git
#### 

# Create repo > Upload files




