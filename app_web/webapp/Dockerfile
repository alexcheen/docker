# Version: 0.0.1


FROM ubuntu:16.04
LABEL author = "Alex Cheen"
ENV REFRESHED_AT 2020-05-15
RUN apt-get update 
RUN apt-get -y install ruby ruby-dev build-essential redis-tools
RUN gem install --no-rdoc --no-ri sinatra json redis

RUN mkdir -p /opt/webapp

EXPOSE 4567

CMD ["/opt/webapp/bin/webapp"]