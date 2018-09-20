ShadowsocksR
===========

[![Build Status]][Travis CI]

A fast tunnel proxy that helps you bypass firewalls.

Server
------

### Install

Debian / Ubuntu:

    apt-get install git
    git clone https://github.com/k2775739/SSR.git

CentOS:

    yum install git
    git clone https://github.com/k2775739/SSR.git

Windows:

    git clone https://github.com/k2775739/SSR.git

### Usage for single user on linux platform

If you clone it into `~/SSR`  
move to `~/SSR`, then run:

    bash initcfg.sh

move to `~/SSR/shadowsocks`, then run:

    python server.py -p 443 -k password -m aes-128-cfb -O auth_aes128_md5 -o tls1.2_ticket_auth_compatible

Check all the options via `-h`.

You can also use a configuration file instead (recommend), move to `~/SSR` and edit the file `user-config.json`, then move to `~/SSR/shadowsocks` again, just run:

    python server.py

To run in the background:

    ./logrun.sh

To stop:

    ./stop.sh

To monitor the log:

    ./tail.sh


Client
------

* [Windows] / [macOS]
* [Android] / [iOS]
* [OpenWRT]

Use GUI clients on your local PC/phones. Check the README of your client
for more information.

Documentation
-------------

You can find all the documentation in the [Wiki].

License
-------

Copyright 2015 clowwindy

Licensed under the Apache License, Version 2.0 (the "License"); you may
not use this file except in compliance with the License. You may obtain
a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
License for the specific language governing permissions and limitations
under the License.


centos7 CHACHA20

        yum install m2crypto gcc -y

        wget -N --no-check-certificate https://github.com/jedisct1/libsodium/releases/download/1.0.8/libsodium-1.0.8.tar.gz

        tar zfvx libsodium-1.0.8.tar.gz

        cd libsodium-1.0.8

        ./configure

        make && make install

        echo "include ld.so.conf.d/*.conf" > /etc/ld.so.conf

        echo "/lib" >> /etc/ld.so.conf

        echo "/usr/lib64" >> /etc/ld.so.conf

        echo "/usr/local/lib" >> /etc/ld.so.conf

        ldconfig




Bugs and Issues
----------------

* [Issue Tracker]



[Android]:           https://github.com/shadowsocksr/shadowsocksr-android
[Build Status]:      https://travis-ci.org/shadowsocksr/shadowsocksr.svg?branch=manyuser
[Debian sid]:        https://packages.debian.org/unstable/python/shadowsocks
[iOS]:               https://github.com/shadowsocks/shadowsocks-iOS/wiki/Help
[Issue Tracker]:     https://github.com/shadowsocksr/shadowsocksr/issues?state=open
[OpenWRT]:           https://github.com/shadowsocks/openwrt-shadowsocks
[macOS]:             https://github.com/shadowsocksr/ShadowsocksX-NG
[Travis CI]:         https://travis-ci.org/shadowsocksr/shadowsocksr
[Windows]:           https://github.com/shadowsocksr/shadowsocksr-csharp
[Wiki]:              https://github.com/breakwa11/shadowsocks-rss/wiki
