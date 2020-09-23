FROM alpine:3.4

RUN apk update                  \
 && apk add socat               \
 &&  rm -rf /var/cache/apk/*

ENV PORT        8080
ENV TARGET      "127.0.0.1:8090"


CMD exec socat -ddd -ls "TCP-LISTEN:$PORT,fork" "TCP:$TARGET"
