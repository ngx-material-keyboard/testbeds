FROM node:8

LABEL authors="David Enke <post@davidenke.de>"

RUN mkdir -p /testbed

WORKDIR /testbed

ADD app /testbed/

VOLUME /testbed

RUN npm install \
    --no-audit \
    --no-optional \
    --no-package-lock \
    --no-progress \
    --loglevel=error \
  && rm -rf /tmp/* *.tar.gz ~/.npm
