# Node.js v4.2 (Long Term Support)
# docker run --rm pottava/nodejs:4.2 node -v

FROM alpine:3.3

ENV NODE_VERSION=4.2.4

RUN apk --no-cache add --virtual build-dependencies build-base linux-headers binutils-gold python curl \
      && mkdir -p /tmp/src \
      && cd /tmp/src \
      && curl --location --silent https://nodejs.org/dist/v${NODE_VERSION}/node-v${NODE_VERSION}.tar.gz | tar xzf - \
      && cd /tmp/src/node-v${NODE_VERSION} \
      && ./configure --prefix=/opt/node \
      && make \
      && make install \
      && cd / && rm -rf /tmp/src \
      && apk del build-dependencies \
      && apk --no-cache add libgcc libstdc++

ENV PATH=${PATH}:/opt/node/bin NODE_PATH=/opt/node/lib/node_modules
