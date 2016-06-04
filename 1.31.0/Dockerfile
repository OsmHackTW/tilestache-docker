FROM osmtw/mapnik2:v2.2.0
MAINTAINER Rex Tsai <rex.cc.tsai@gmail.com>

ENV TILESTACHE_VERSION=1.31.0-1ubuntu1 \
    UWSGI_VERSION=1.9.17.1-5build5

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update \
 && apt-get install -y tilestache=$TILESTACHE_VERSION \
        uwsgi=$UWSGI_VERSION uwsgi-plugin-python=$UWSGI_VERSION

# Clean up APT when done
RUN apt-get clean \
 && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
