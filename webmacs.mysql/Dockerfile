FROM linuxserver/mariadb:arm32v7-latest

# Install extra system packages
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash - && \
    apt-get update && \
    apt-get install --no-install-recommends -y \
    unzip && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

COPY custom.cnf /etc/test/custom.cnf
COPY ./custom.cnf /etc/mysql/conf.d/custom.cnf

