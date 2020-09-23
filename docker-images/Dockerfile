FROM alpine:3.4

RUN apk update                  \
 && apk add socat               \
 &&  rm -rf /var/cache/apk/*

ENV PORT        1234
ENV TARGET      "127.0.0.1:2345"


CMD exec socat -ddd -ls "TCP-LISTEN:$PORT,fork" "TCP:$TARGET"
