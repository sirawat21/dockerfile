FROM ubuntu:latest
LABEL maintainer "Best Sira <sirawat21@gmail.com>"
RUN apt-get update -y \
    && ap-get install -y git npm nodejs
RUN npm update \
    && npm insall -g nodemon \
    && npm install
WORKDIR /www
