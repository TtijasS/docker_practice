FROM ubuntu:latest

# Update packages and apache2
RUN apt-get update && apt-get install -y apache2 nano

# Expose default apache port
EXPOSE  80

# Run ssh daemon in forground to prevent container from exiting
CMD ["apache2ctl", "-D", "FOREGROUND"]