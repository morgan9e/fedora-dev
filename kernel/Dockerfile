FROM registry.fedoraproject.org/fedora-toolbox:43

RUN dnf update -y

RUN dnf builddep -y kernel

RUN dnf install -y \
    fedpkg fedora-packager rpmdevtools pesign git \
    bpftool bc bison dwarves elfutils-devel elfutils-libelf-devel flex \
    gcc gcc-c++ gcc-plugin-devel glibc-static hostname m4 make \
    net-tools openssl openssl-devel perl-devel perl-generators \
    python3-devel which kernel-rpm-macros vim \
    audit-libs-devel binutils-devel java-devel kabi-dw \
    libcap-devel libcap-ng-devel llvm-devel newt-devel \
    numactl-devel pciutils-devel python3-docutils \
    "perl(ExtUtils::Embed)" systemd-devel xmlto \
    libbpf-devel rsync hmaccalc ncurses-devel \
    curl wget tar gzip bzip2 xz zstd zip unzip \
    clang lld llvm compiler-rt ccache perl \
    && dnf clean all

RUN mkdir -p /data
WORKDIR /data

CMD ["/bin/bash"]
