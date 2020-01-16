FROM ubuntu:latest
LABEL maintainer "Best Sira <sirawat21@gmail.com>"
RUN apt-get update -y \
    && apt-get install -y git npm nodejs \
    && rm -rf /var/lib/apt/lists/*
    && npm update \
    && npm insall -g nodemon \
    && npm install
VOLUME ["/www"]
WORKDIR /www
EXPOSE 80 443
