FROM jenkins/jenkins:lts
LABEL maintainer "Michael Prinsloo (github.com/prinsmike)"
LABEL version "1.0"
LABEL date "2018-06-09"

VOLUME ["/var/jenkins_home", "/data"]

COPY plugins.txt /usr/share/jenkins/ref/plugins.txt

RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt

USER root

RUN mkdir -p /data

USER jenkins
