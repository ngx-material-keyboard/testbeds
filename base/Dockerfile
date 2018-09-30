FROM node:8

LABEL authors="David Enke <post@davidenke.de>"

# credits to https://github.com/emmenko/docker-nodejs-karma

RUN curl https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add - \
    && sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list' \
    && apt-get update
    && apt-get install -y Xvfb google-chrome-stable \
    && apt-get clean
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

ADD prepare_testbed.sh /bin/prepare_testbed.sh

RUN chmod a+x /bin/prepare_testbed.sh
