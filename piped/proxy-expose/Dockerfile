FROM alpine:3.14

RUN apk update && \
    apk upgrade && \
    apk add --no-cache socat

EXPOSE 12345/tcp

ENTRYPOINT ["socat", "TCP-LISTEN:12345,reuseaddr,fork", "UNIX-CLIENT:/app/socket/actix.sock"]
