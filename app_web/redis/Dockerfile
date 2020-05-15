FROM ubuntu:16.04
LABEL author="Alex Cheen"
ENV REFRESHED_AT 2020-05-15

RUN apt-get -qq update && apt-get -qq install redis-server redis-tools

EXPOSE 6379

ENTRYPOINT ["/usr/bin/redis-server" ]
CMD []