# Node.js v5.4
# docker run --rm pottava/nodejs:5.4 node -v

FROM alpine:3.3

ENV NODE_VERSION=5.4.1

RUN apk --no-cache add --virtual build-dependencies make gcc g++ linux-headers binutils-gold python curl \
      && apk --no-cache add libgcc libstdc++ \
      && mkdir -p /tmp/src \
      && cd /tmp/src \
      && curl --location --silent https://nodejs.org/dist/v${NODE_VERSION}/node-v${NODE_VERSION}.tar.gz | tar xzf - \
      && cd /tmp/src/node-v${NODE_VERSION} \
      && ./configure --prefix=/opt/node \
      && make \
      && make install \
      && cd / && rm -rf /tmp/src \
      && apk del build-dependencies

ENV PATH=${PATH}:/opt/node/bin NODE_PATH=/opt/node/lib/node_modules
