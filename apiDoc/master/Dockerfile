FROM node:0.11
MAINTAINER Baptiste Donaux <baptiste.donaux@gmail.com>

RUN npm install apidoc -g

ENV INPUT /home/docker
ENV OUTPUT /home/docker/doc

USER 1000
WORKDIR /home/docker
CMD apidoc -f '.*\.php$' -i $INPUT -o $OUTPUT
