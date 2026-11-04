FROM postgis/postgis:14-3.1

RUN sed -i 's|apt.postgresql.org/pub/repos/apt|apt-archive.postgresql.org/pub/repos/apt|g' /etc/apt/sources.list.d/pgdg.list \
    && sed -i \
       -e 's|deb.debian.org/debian|archive.debian.org/debian|g' \
       -e 's|security.debian.org/debian-security|archive.debian.org/debian-security|g' \
       -e '/bullseye-updates/d' \
       /etc/apt/sources.list \
    && apt-get -o Acquire::Check-Valid-Until=false update \
    && apt-get -y install --no-install-recommends \
       unzip \
       curl \
       wget \
       postgis \
       osm2pgsql

WORKDIR /work
