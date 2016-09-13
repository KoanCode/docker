FROM koancode/gwt:latest

# Build that has a cache from gradle so it does not download the internet each build

MAINTAINER Ryan Mills <ryan@koancode.com>

RUN mkdir ~/.gradle
# copy cannot use ~ link, so use root
COPY caches /root/.gradle/caches/

CMD ['/bin/bash']