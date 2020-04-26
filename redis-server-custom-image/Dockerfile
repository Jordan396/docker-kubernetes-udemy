# Use an existing docker image as a base
FROM alpine

# Download and install a dependency
RUN echo http://mirror.yandex.ru/mirrors/alpine/v3.5/main > /etc/apk/repositories;
RUN echo http://mirror.yandex.ru/mirrors/alpine/v3.5/community >> /etc/apk/repositories

RUN apk update && apk add --no-cache
RUN apk add --update redis

# Tell image what to do when it starts as a container
CMD [ "redis-server" ]