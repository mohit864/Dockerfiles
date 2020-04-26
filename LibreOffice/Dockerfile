# USAGE:
#
#   # To Download libreoffice Dockerfile
#       wget https://raw.githubusercontent.com/mohitdhule/Dockerfiles/master/LibreOffice/Dockerfile
# 	
#   # To Build libreoffice image
#	docker build -t libreoffice .
#
#   # To Run libreoffice image
#	docker run -d \
#                -v /tmp/.X11-unix:/tmp/.X11-unix \
#		 -e DISPLAY=unix$DISPLAY
#		 -v /home/mohitdhule/Documents:/home/libreoffice \
#                libreoffice
#

FROM alpine
LABEL maintainer "Mohit Dhule <mohitdhule@outlook.com>"

RUN apk add --no-cache \
    --repository http://dl-cdn.alpinelinux.org/alpine/edge/testing \
    libreoffice ttf-dejavu && \
    adduser --disabled-password --gecos "" libreoffice

VOLUME /home/libreoffice

USER libreoffice
WORKDIR /home/libreoffice

ENTRYPOINT ["libreoffice"]


