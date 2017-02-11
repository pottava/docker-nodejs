# Node.js v6.9
# docker run --rm pottava/nodejs:6.9 node -v
# docker run --rm pottava/nodejs:6.9 npm -v

FROM alpine:3.5

ENV NPM_CONFIG_LOGLEVEL=info \
    NODE_VERSION=6.9.5-r0

RUN apk --no-cache add ca-certificates \
 && apk --no-cache add nodejs=$NODE_VERSION
