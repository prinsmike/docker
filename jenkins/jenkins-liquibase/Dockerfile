FROM jenkins/jenkins:lts
LABEL maintainer "Michael Prinsloo (github.com/prinsmike)"

VOLUME ["/var/jenkins_home", "/data", "/changesets"]

COPY plugins.txt /usr/share/jenkins/ref/plugins.txt

RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt

USER root

RUN mkdir -p /changesets /data

USER jenkins
