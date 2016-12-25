FROM ubuntu
MAINTAINER noeyhjun kim <kane7274@gmail.com>

# Fix sh
RUN rm /bin/sh && ln -s /bin/bash /bin/sh

# Install dependencies
RUN apt-get update && \
apt-get install -y git apt-utils  build-essential curl wget software-properties-common openssh-server

# Install Node.js 6.x 
RUN  curl -sL https://deb.nodesource.com/setup_6.x | bash - && \
apt-get install -y nodejs

# add user and working directory make
ENV HOME_PATH home/service

# Important! : You should change passwd. (default xhazot)
RUN adduser --disabled-password --gecos "" jenkins \
&& echo 'jenkins:guswns12' | chpasswd \
&& mkdir /${HOME_PATH} \
&& mkdir /${HOME_PATH}/tmp \
&& mkdir /var/run/sshd

ENV NODE_ENV production

EXPOSE 22
EXPOSE 3000

# Launch sshd
CMD ["/usr/sbin/sshd", "-D"]