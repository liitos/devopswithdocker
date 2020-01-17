FROM ubuntu:16.04 as build-stage
RUN mkdir -p /usr/app
WORKDIR /usr/app
RUN apt-get update && apt-get install -y curl
COPY frontend-example-docker . 
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN node -v
RUN npm -v
RUN npm install
RUN npm run build
FROM node:alpine
RUN mkdir -p /usr/app
WORKDIR /usr/app
COPY --from=build-stage /usr/app/dist /usr/app/dist
RUN apk add --no-cache curl && npm install -g serve && adduser -D app && chown -R app:app /usr/app/
USER app
ENV API_URL=http://localhost:8000
CMD serve -s -l 8000 dist
