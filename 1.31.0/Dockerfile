FROM osmtw/mapnik2:v2.2.0
MAINTAINER Rex Tsai <rex.cc.tsai@gmail.com>

ENV DEBIAN_FRONTEND=noninteractive \
    TILESTACHE_VERSION=1.31.0-1ubuntu1 \
    _UWSGI_VERSION_=1.9.17.1-5build5
RUN apt-get update \
 && apt-get dist-upgrade -y \
 && apt-get install -y tilestache=$TILESTACHE_VERSION \
        uwsgi=$_UWSGI_VERSION_ uwsgi-plugin-python=$_UWSGI_VERSION_

# Clean up APT when done
RUN apt-get clean \
 && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
