FROM ubuntu:16.04 
RUN mkdir -p /usr/app
WORKDIR /usr/app
RUN apt-get update && apt-get install -y curl  
COPY doCurl.sh . 
RUN chmod +x doCurl.sh 
CMD ["/bin/bash", "/usr/app/doCurl.sh"]
