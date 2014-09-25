FROM ubuntu:14.04

MAINTAINER Maksym Bodnarchuk <bodnarchuk@gmail.com>

ENV REFRESHED_AT 2014-09-25

RUN apt-get update
RUN apt-get install -y build-essential curl

RUN curl https://raw.githubusercontent.com/creationix/nvm/v0.17.0/install.sh | bash
RUN echo ". /.nvm/nvm.sh" >> /etc/bash.bashrc
RUN /bin/bash -c '. /.nvm/nvm.sh && nvm install 0.10 && nvm use 0.10 && nvm alias default 0.10'

VOLUME ["/draft"]

WORKDIR /draft

CMD ["/bin/bash"]
