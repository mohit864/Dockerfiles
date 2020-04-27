# USAGE:
#
#   # To Download gparted Dockerfile
#       wget https://raw.githubusercontent.com/mohitdhule/Dockerfiles/master/GParted/Dockerfile
# 	
#   # To Build gparted image
#	docker build -t gparted .
#
#   # To Run gparted image
#	docker run -d \
#                -v /tmp/.X11-unix:/tmp/.X11-unix \
#		 -e DISPLAY=unix$DISPLAY \
#		 --device=/dev/sda:/dev/sda \
#                --device=/dev/mem:/dev/mem \
#                gparted
#

FROM debian:stable-slim

RUN apt update -y && apt install -y \
    gparted dosfstools libcanberra-gtk-module && \
    apt clean

ENTRYPOINT ["gparted"]


