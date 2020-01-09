FROM ubuntu:16.04 
RUN mkdir -p /usr/app
WORKDIR /usr/app
RUN apt-get update && apt-get install -y curl
COPY frontend-example-docker . 
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN node -v
RUN npm -v 
WORKDIR /usr/app/frontend-example-docker
ENV API_URL=http://193.65.107.254:8000
RUN npm install
CMD npm start
