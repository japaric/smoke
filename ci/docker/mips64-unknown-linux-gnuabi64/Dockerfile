FROM ubuntu:16.10
RUN apt-get update
RUN apt-get install -y --no-install-recommends \
    ca-certificates \
    gcc \
    gcc-mips64-linux-gnuabi64 \
    libc6-dev \
    libc6-dev-mips64-cross \
    qemu-user-static
RUN apt-get install -y --no-install-recommends qemu-system-mips
ENV CARGO_TARGET_MIPS64_UNKNOWN_LINUX_GNUABI64_LINKER=mips64-linux-gnuabi64-gcc \
    CC_mips64_unknown_linux_gnuabi64=mips64-linux-gnuabi64-gcc \
    QEMU_LD_PREFIX=/usr/mips64-linux-gnuabi64 \
    RUST_TEST_THREADS=1
