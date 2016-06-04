FROM osmtw/mapnik3:v3.0.11
MAINTAINER Rex Tsai <rex.cc.tsai@gmail.com>

ENV TILESTACHE_VERSION=1.49.8-3 \
    UWSGI_VERSION=2.0.12-5ubuntu3

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update \
 && apt-get install -y tilestache=$TILESTACHE_VERSION \
        uwsgi=$UWSGI_VERSION uwsgi-plugin-python=$UWSGI_VERSION

# Clean up APT when done
RUN apt-get clean \
 && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
