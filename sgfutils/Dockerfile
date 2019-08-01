# Run sgfutils:
#   docker run -v $(pwd):/sgfutils -it sgfutils
FROM ubuntu:latest
RUN apt-get -y update
RUN apt-get -y install curl
RUN apt-get -y install build-essential
RUN apt-get -y install libssl-dev
RUN curl https://homepages.cwi.nl/~aeb/go/sgfutils/sgfutils.tgz -o sgfutils.tgz
RUN gzip -d sgfutils.tgz
RUN tar -xvf sgfutils.tar
RUN cd sgfutils-* && make
RUN cp sgfutils-*/sgf* /usr/local/bin
WORKDIR /sgfutils
CMD ["/bin/bash"]
