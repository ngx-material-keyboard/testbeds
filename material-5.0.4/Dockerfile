FROM ngxmaterialkeyboard/testbeds:base

LABEL authors="David Enke <post@davidenke.de>"

RUN apk update \
  && npm install @angular/cli@1.7.4 \
  && rm -rf /tmp/* /var/cache/apk/* *.tar.gz ~/.npm \
  && npm cache clear --force
