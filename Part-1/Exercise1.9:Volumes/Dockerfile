FROM ubuntu:18.04

WORKDIR /Volumes/Battuta/Developer/UoHDataScience/DevOps-Docker/DevOps-Docker/Part-1/Exercise1.8:Image-for-script/

RUN apt-get update && apt-get install -y curl python
RUN curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl
RUN chmod a+x /usr/local/bin/youtube-dl
RUN youtube-dl https://imgur.com/JY5tHqr
#RUN cp "/Volumes/Battuta/Developer/UoHDataScience/DevOps-Docker/DevOps-Docker/Part-1/Exercise1.9:Volumes/Imgur-JY5tHqr.mp4" .

ENV LC_ALL=C.UTF-8

ENTRYPOINT ["/usr/local/bin/youtube-dl"]
