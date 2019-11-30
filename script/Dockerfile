FROM debian:latest
WORKDIR /elementary_os
COPY ./ /elementary_os
RUN chmod -R +x /elementary_os/*
RUN /bin/bash /elementary_os/build.sh