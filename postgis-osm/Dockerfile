FROM postgis/postgis:16-3.6

RUN apt-get update \
    && apt-get -y install --no-install-recommends \
    ca-certificates \
    unzip \
    curl \
    wget \
    osm2pgsql \
    postgis

WORKDIR /work
