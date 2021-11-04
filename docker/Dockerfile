FROM alpine:20210804

RUN addgroup -g 1000 cppdev \
  && adduser -u 1000 -G cppdev -h /home/cppdev -D cppdev

RUN apk add \
    neovim \
    neovim-doc \
    llvm12 \
    clang \
    clang-analyzer \
    clang-extra-tools \
    clang-doc \
    ctags \
    ctags-doc \
    lldb \
    cmake \
    cmake-doc \
    samurai \
    samurai-doc \
    git \
    git-doc \
    curl \
    curl-doc \
    ncurses \
    ncurses-terminfo \
    ncurses-doc \
    screen \
    screen-doc \
    gawk \
    gawk-doc

WORKDIR /home/cppdev

USER cppdev

RUN mkdir -p /home/cppdev/.ssh \
  && chmod 0700 /home/cppdev/.ssh

LABEL maintainer=MetaBarj0
LABEL role=cpp-ide
