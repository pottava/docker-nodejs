# Node.js v6.10
# docker run --rm pottava/nodejs:6.10 node -v
# docker run --rm pottava/nodejs:6.10 npm -v

FROM alpine:edge

ENV NPM_CONFIG_LOGLEVEL=info \
    NODE_VERSION=6.10.1-r0

RUN apk --no-cache add ca-certificates \
 && apk --no-cache add nodejs=$NODE_VERSION
