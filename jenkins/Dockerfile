FROM jenkins/jenkins:lts

ENV DEBIAN_FRONTEND noninteractive

USER root

RUN apt-get update -y && apt-get install -y sudo && apt install wget
&& curl -fL -o docker.tgz "https://download.docker.com/linux/static/test/x86_64/docker-19.03.9.tgz" \
&& tar --strip-components=1 -xvzf docker.tgz -C /usr/bin \
&& gpasswd -a jenkins root 
&& sudo wget http://54.249.160.239:8080/jnlpJars/jenkins-cli.jar

RUN apt-get update \
  && apt-get install -y \
  nodejs  \
  npm \
  libgtk2.0-0 \
  libgtk-3-0 \
  libgbm-dev \
  libnotify-dev \
  libgconf-2-4 \
  libnss3 \
  libxss1 \
  libasound2 \
  libxtst6 \
  xauth \
  xvfb

RUN sudo apt-get update && sudo apt-get install awscli


USER jenkins
