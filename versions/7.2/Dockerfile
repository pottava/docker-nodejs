# Node.js v7.2
# docker run --rm pottava/nodejs:7.2 node -v
# docker run --rm pottava/nodejs:7.2 npm -v

FROM alpine:3.5

ENV NPM_CONFIG_LOGLEVEL=info \
    NODE_VERSION=7.2.1-r0

RUN apk --no-cache add ca-certificates \
 && apk --no-cache add nodejs-current=$NODE_VERSION
