FROM registry.fedoraproject.org/fedora-toolbox:43

RUN dnf update -y && \
    dnf builddep -y --setopt=install_weak_deps=False kernel && \
    dnf install -y --setopt=install_weak_deps=False \
        clang lld llvm compiler-rt ccache perl && \
    dnf clean all

CMD ["/bin/bash"]
