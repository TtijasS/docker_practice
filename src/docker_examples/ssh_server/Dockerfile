FROM ubuntu:latest

WORKDIR /app

# Update packages and install openssh-server and nano
RUN apt-get update && apt-get install -y openssh-server nano

# Make sure the dir exists
RUN mkdir -p /var/run/sshd

# Set root password
RUN echo 'root:password' | chpasswd

# Allow root login via ssh
RUN sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config

# Expose default ssh port 22
EXPOSE  22

# Run ssh daemon in forground to prevent container from exiting
CMD ["/usr/sbin/sshd", "-D"]