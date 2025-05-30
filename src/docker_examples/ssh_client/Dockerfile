FROM ubuntu:latest

WORKDIR /app

# Update packages and install openssh-server and nano
RUN apt-get update && apt-get install -y openssh-client nano

# Run ssh daemon in forground to prevent container from exiting
CMD ["/bin/bash"]