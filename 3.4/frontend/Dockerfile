FROM node:alpine
RUN mkdir -p /usr/app
WORKDIR /usr/app
COPY frontend-example-docker /usr/app/ 
RUN apk add --no-cache curl && npm install && adduser -D app && chown -R app:app /usr/app/
USER app
#WORKDIR /usr/app/frontend-example-docker
ENV API_URL=http://node2.liitos.biz:8000
CMD npm start
