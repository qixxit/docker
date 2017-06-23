FROM leifg/elixir:1.4.5
MAINTAINER Leif Gensert <leif@leif.io>

RUN apk add --no-cache git build-base tar git openssh

RUN mkdir -p /aws \
	&& apk -Uuv add groff less python py-pip \
  && pip install --upgrade pip \
	&& pip install awscli \
	&& apk --purge -v del py-pip \
	&& rm /var/cache/apk/*
