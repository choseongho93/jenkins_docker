# jenkins_docker
Linux OS (Centos, ubuntu) Dockerfile 

## content
UPDATED to wget the latest available war file at build time.

With docker installed and the git repo checked out to the current directory, you can build this image like this:

docker build -t jenkins:latest .

and run it with these args:

docker run --name jenkins -v /var/jenkins_home:/var/jenkins_home -e TZ=Asia/Seoul -d -p 8080:8080 jenkins:latest

where:

-p 8080:8080 maps the host to container port 8080.

(You can add 5000 for slave nodes too)

-v /var/jenkins_home:/var/jenkins_home maps some local host dir to the containers JENKINS_HOME in /var/jenkins_home

TODO:

sort out running as the jenkins user and mapping the data volume at the same time


