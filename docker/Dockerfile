FROM docker/compose:1.18.0

RUN apk update \
  && apk upgrade \
  && apk add ruby docker bash

RUN mkdir /config

ADD nginx.conf /
ADD uploadsize.conf /
ADD cloud.yaml.erb /
ADD generate-config.rb /
ADD run.sh /

RUN chmod +x /run.sh

ENTRYPOINT /run.sh
