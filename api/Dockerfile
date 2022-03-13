# Specify a base image
FROM ubuntu:18.04
RUN apt-get update && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_14.x | bash -
RUN apt-get update && apt-get install -y nodejs

#Install some dependencies

WORKDIR /usr/app_server
COPY ./ /usr/app_server
RUN npm install
EXPOSE 4000
# Set up a default ciommand
CMD [ "npm","start" ]