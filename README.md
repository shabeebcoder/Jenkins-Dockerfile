<h1>Build docker image with Jenkins, ansible </h1>

FROM jenkins/jenkins
USER root
RUN apt-get update
RUN apt-get install -y ansible
USER jenkins


docker build -t jenkins .

RUN Docker container 
docker run -p 8080:8080 -p 50000:50000 -v ~/jenkins_home:/var/jenkins_home jenkins