FROM debian:stable

WORKDIR /var/www

RUN apt-get update && \
    apt-get -y --no-install-recommends install curl \
        ca-certificates && \
    curl https://raw.githubusercontent.com/gadiener/docker-images-size-benchmark/master/main.go -o main.go && \
    apt-get purge -y curl \
        ca-certificates && \
    apt-get autoremove -y && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
