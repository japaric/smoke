FROM ubuntu:16.10
RUN apt-get update
RUN apt-get install -y --no-install-recommends \
    ca-certificates \
    curl \
    gcc \
    gcc-arm-none-eabi \
    libc6-dev \
    libnewlib-dev
RUN curl -LSfs http://japaric.github.io/trust/install.sh | \
    sh -s -- --git japaric/xargo --tag v0.2.0 --target x86_64-unknown-linux-gnu --to /usr/bin
