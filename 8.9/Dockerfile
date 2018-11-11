FROM debian:stretch-slim

WORKDIR /var/www

RUN /bin/bash -c  "apt-get update \
    && apt-get install -y wget libpng* build-essential gcc make autoconf libtool pkg-config nasm \
    && wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash \
    && source /root/.bashrc \
    && cd /root \
    && nvm install 8.9"

COPY entrypoint.sh /entrypoint.sh

RUN chmod +x /entrypoint.sh

CMD ["/entrypoint.sh"]