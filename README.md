FROM ubuntu:22.04

# Set temp work directory
# for package configuration
#WORKDIR usrsrccache

# Update apt packages
RUN apt update
RUN apt install -y ffmpeg

# Install vim
#RUN apt install vim -y

# Install python 3.11
RUN apt-get install -y python3

# Install pip
RUN apt install python3-pip -y
    pip install --upgrade pip

# Install  Auto-Editor
RUN pip install auto-editor

# Export
RUN auto-editor 1.mp4 --export resolve

# Install lsof
#RUN apt install lsof

## Set working directory for code
#WORKDIR usrsrcapp# autocut
