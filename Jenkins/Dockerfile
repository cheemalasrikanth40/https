FROM ubuntu:20.04 AS java
ENV DEBIAN_FRONTEND noninteractive
RUN apt update && apt install -y sudo openjdk-8-jdk git maven gnupg wget -y
RUN apt update && wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add - &&\
    sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list' &&\
    apt update &&\
    apt install jenkins gnupg2 -y

#COPY startup.sh /
#ENTRYPOINT ["/startup.sh"]
