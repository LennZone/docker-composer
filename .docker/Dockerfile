FROM php:8.3-apache AS Base

RUN apt-get update &&\
    apt-get upgrade -y &&\
    apt-get install -y  \
    nano \
    git  \
    unzip \
    npm &&\
    apt-get clean &&\
    rm -rf /var/lib/apt/lists/*

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN echo " \
    export LS_OPTIONS='--color=auto' \n \
    alias ls='ls \$LS_OPTIONS' \n \
    alias ll='ls \$LS_OPTIONS -la' \n \
    alias l='ls \$LS_OPTIONS -lA' \n \
    alias rm='rm -i' \n \
    alias cp='cp -i' \n \
    alias mv='mv -i' \n " >> /etc/bash.bashrc