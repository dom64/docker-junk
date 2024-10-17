FROM alpine:latest

RUN echo 'http://mirrors.edge.kernel.org/alpine/latest-stable/community' >> /etc/apk/repositories
RUN apk update && apk add openjdk21 && apk add libstdc++

EXPOSE 25565

COPY init.sh /

RUN chmod +x init.sh

RUN mkdir /minecraft

CMD ./init.sh