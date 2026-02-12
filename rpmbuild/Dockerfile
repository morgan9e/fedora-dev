FROM registry.fedoraproject.org/fedora-toolbox:43

RUN dnf update -y && \
    dnf install -y --setopt=install_weak_deps=False \
    fedpkg fedora-packager rpmdevtools rpm-build rpm-sign pesign \
    gcc gcc-c++ make cmake autoconf automake libtool \
    openssl-devel elfutils-devel ncurses-devel \
    curl wget \
    tar gzip bzip2 xz zstd \
    git vim \
    && dnf clean all

RUN rpmdev-setuptree

WORKDIR /root/rpmbuild

CMD ["/bin/bash"]
