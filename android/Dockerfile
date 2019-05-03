FROM circleci/android:api-28
MAINTAINER daniel@qixxit.de

USER root
RUN apt-get update && apt-get install --no-install-recommends -y ruby ruby-dev build-essential \
	&& gem install fastlane --no-document --quiet \
	&& apt-get autoremove -y && rm -rf /var/lib/apt/lists/*
USER circleci
