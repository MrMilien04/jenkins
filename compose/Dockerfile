FROM jenkins/jenkins:latest

USER root
RUN apt-get update && apt-get install -y maven
USER jenkins
RUN jenkins-plugin-cli --plugins "git"