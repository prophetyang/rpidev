#
# Ubuntu Dockerfile
#
# https://github.com/dockerfile/ubuntu
#

# Pull base image.
FROM ubuntu:14.04

# Install.
RUN \
	apt-get update -y && \
	apt-get upgrade -y && \
	apt-get install -y build-essential && \
	apt-get install -y software-properties-common && \
	apt-get install -y git unzip vim wget && \
	rm -rf /var/lib/apt/lists/*

ENV WORKSPACE /workspace
RUN \
	mkdir $WORKSPACE && \
	cd $WORKSPACE && \
	git clone https://github.com/raspberrypi/tools

ENV HOME /root

# Define default command.
CMD ["bash"]
