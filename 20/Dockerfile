FROM ubuntu:20.04

RUN apt-get update && apt-get install -y openssh-client && apt-get install -y openssh-server && apt-get install net-tools

RUN useradd -rm -d /home/ubuntu -s /bin/bash -g root -G sudo -u 1000 test 

RUN  echo 'test:test' | chpasswd

RUN service ssh start

EXPOSE 22

CMD ["/usr/sbin/sshd","-D"]