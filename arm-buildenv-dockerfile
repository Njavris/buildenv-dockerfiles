FROM ubuntu:24.04

# Noninteractive frontend so tzdata doesn't block
ENV DEBIAN_FRONTEND=noninteractive

# Install dependencies
RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
    wget \
    bc \
    libssl-dev \
    libncurses-dev \
    libncurses5-dev \
    python3 \
    python3-pip \
    ca-certificates \
    u-boot-tools \
    device-tree-compiler \
    git \
    ssh \
    make \
    gcc \
    liblz4-tool \
    expect \
    expect-dev \
    g++ \
    patchelf \
    chrpath \
    gawk \
    texinfo \
    chrpath \
    diffstat \
    binfmt-support \
    qemu-user-static \
    live-build \
    bison \
    flex \
    fakeroot \
    cmake \
    gcc-multilib \
    g++-multilib \
    unzip \
    ncurses-dev \
    libgucharmap-2-90-dev \
    bzip2 \
    expat \
    gnupg \
    cpp-aarch64-linux-gnu \
    libgmp-dev \
    libmpc-dev \
    python-is-python3 \
    module-assistant \
    gperf \
    autoconf \
    pkg-config \
    passwd \
    openssl \
    openssh-server \
    openssh-client \
    vim \
    file \
    cpio \
    rsync \
    curl \
    && rm -rf /var/lib/apt/lists/*

# Install ARMv7 cross toolchain (gcc-arm-none-eabi or GCC cross)
# gcc-arm-linux-gnueabihf = correct for Linux userspace (kernel+uboot)
RUN apt-get update && apt-get install -y gcc-arm-linux-gnueabihf \
    && rm -rf /var/lib/apt/lists/*

# Create a workspace
RUN mkdir -p /home/build
WORKDIR /home/build

# Default command
CMD ["/bin/bash"]

