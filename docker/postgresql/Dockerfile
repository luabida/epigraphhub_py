FROM postgis/postgis:14-3.2

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get -qq update --yes \
  && apt-get -qq install --yes --no-install-recommends \
  build-essential ca-certificates \
  postgresql-14-plr \
  # postgresql-14-postgis-3-scripts \
  postgresql-plpython3-14 \
  postgresql-contrib \
  wget \
  && rm -rf /var/lib/apt/lists/*


RUN wget http://ftp.de.debian.org/debian/pool/main/p/postgis/postgresql-14-postgis-3-scripts_3.3.0+dfsg-1_all.deb \
  && chmod +x postgresql-14-postgis-3-scripts_3.3.0+dfsg-1_all.deb \
  && dpkg -i postgresql-14-postgis-3-scripts_3.3.0+dfsg-1_all.deb
