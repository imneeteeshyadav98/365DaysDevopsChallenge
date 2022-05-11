### Docker security 
### Solveing simple use case how to secure your docker images.
##### How to disable root login in container ?.
### Creating Dockerfile like this...
FROM ubuntu 
LABEL maintainer="neeteeshyadav98@gmail.com"
RUN groupadd -r  neetesh && useradd -r  -g neetesh neetesh
RUN chsh -s /usr/sbin/nologin root
USER neetesh
ENV HOME /home/neetesh
ENV DEBIAN_FRONTEND=noninteractive



