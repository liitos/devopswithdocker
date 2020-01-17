FROM ubuntu:16.04 
ENV LC_ALL=C.UTF-8 
RUN apt-get update && apt-get install -y python3 ca-certificates python3-pip ffmpeg wget && rm -rf /var/lib/apt/lists/* && pip3 install --user --upgrade yle-dl
WORKDIR /video 
ENTRYPOINT ["/root/.local/bin/yle-dl"] 
