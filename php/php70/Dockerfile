FROM php:7.0-fpm



COPY ./sources.list.stretch /etc/apt/sources.list
RUN apt-get update
RUN apt-get install -y git gcc make re2c libpcre3-dev

RUN git clone --depth=1 "git://github.com/phalcon/cphalcon.git"
RUN cd cphalcon/build && ./install

RUN git clone git://github.com/phalcon/php-zephir-parser.git
RUN cd php-zephir-parser && ./install

RUN  git clone git://github.com/phalcon/zephir.git
RUN cd zephir && ./install-nosudo && cp ~/bin/zephir /usr/bin/zephir


