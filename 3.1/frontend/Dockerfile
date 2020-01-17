FROM ubuntu:16.04 
RUN mkdir -p /usr/app
WORKDIR /usr/app
COPY frontend-example-docker . 
RUN apt-get update && apt-get install -y curl && curl -sL https://deb.nodesource.com/setup_10.x | bash && apt-get install -y nodejs && npm install && apt-get purge -y --auto-remove curl && rm -rf /var/lib/apt/lists/*
WORKDIR /usr/app/frontend-example-docker
ENV API_URL=http://localhost:8000
CMD npm start
