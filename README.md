## docker-pipeline
## docker-pipeline steps by steps

#### Open the online FREE playground
https://labs.play-with-docker.com/

docker run -d -u root --name jenkins -p 8080:8080 -p 50000:50000 -v /root/jenkins_2112:/var/jenkins_home -v $(which docker):/usr/bin/docker -v /var/run/docker.sock:/var/run/docker.sock --restart always jenkins/jenkins:lts

## Get password
docker exec -it jenkins cat /var/jenkins_home/secrets/initialAdminPassword

## Install ansible
docker exec -it jenkins bash
apt update; apt install python ansible openssh-client vim iputils-ping -y

# Plugins
1. CloudBees Docker Build and Publish plugin
2. Docker Pipeline 
3. Docker

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
#### Repository Url > https://github...git


# Create repo > Upload files

# Jenkinsfile

'''

node {

    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'dockerHub') {

        def customImage = docker.build("mydevopsacademy/dockenodejsrwebapp")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}

'''




