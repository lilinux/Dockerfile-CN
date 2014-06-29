FROM wordpress:latest
MAINTAINER powellli <powellli@tencent.com>

RUN apt-get -y update
RUN apt-get -y install subversion
RUN mkdir /usr/src/wordpress/wp-content/languages
RUN svn export http://i18n.svn.wordpress.org/zh_CN/trunk/messages/zh_CN.mo /usr/src/wordpress/wp-content/languages
RUN sed -i "s/define('WPLANG', '');/define('WPLANG', 'zh_CN');/" /usr/src/wordpress/wp-config-sample.php
