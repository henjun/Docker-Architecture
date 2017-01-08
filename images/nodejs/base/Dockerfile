FROM debian:wheezy
MAINTAINER noeyhjun <kane7274@gmail.com>

RUN apt-get update -y && apt-get install --no-install-recommends -y -q curl python build-essential git ca-certificates

# Install Node.js 6.x
RUN curl -sL https://deb.nodesource.com/setup_6.x | bash - && \
apt-get install -y nodejs