FROM ubuntu
MAINTAINER matt "183299671@qq.com"
ENV REFRESHED_AT 2017-3-20

RUN apt-get clean 
RUN apt-get update
RUN apt-get update  -o Acquire::No-Cache=True
RUN apt-get update  -o Acquire::BrokenProxe=True

RUN apt-get -y install ruby2.3
RUN apt-get -y install ruby-dev
# build-essential 所需的依赖
# RUN apt-get -y install crossbuild-essential-arm64
# RUN apt-get -y install crossbuild-essential-armhf
# RUN apt-get -y install crossbuild-essential-powerpc
# RUN apt-get -y install crossbuild-essential-ppc64el
# RUN apt-get -y install devscripts
# RUN apt-get -y install crossbuild-essential-armel
# RUN apt-get -y install crossbuild-essential-s390x
# RUN apt-get -y install dh-buildinfo
# RUN apt-get -y install sbuild
RUN apt-get update --fix-missing
RUN apt-get -y install build-essential

RUN apt-get -y install redis-tools
RUN gem install --no-rdoc --no-ri sinatra json redis

RUN mkdir -p /opt/webapp

EXPOSE 4567

CMD ["/opt/webapp/bin/webapp"]
