FROM node:alpine
RUN mkdir -p /usr/app
WORKDIR /usr/app
COPY backend-example-docker . 
RUN apk add --no-cache curl && npm install && adduser -D app  && chown -R app:app /usr/app/
USER app
##WORKDIR /usr/app/backend-example-docker
ENV FRONT_URL=http://node1.liitos.biz:5000
CMD npm start
