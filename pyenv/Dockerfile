FROM ubuntu:22.04

WORKDIR /app

RUN apt-get update && apt-get install -y \
    make build-essential libssl-dev zlib1g-dev libbz2-dev \
    libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \
    xz-utils tk-dev libffi-dev liblzma-dev python-openssl git && \
    rm -rf /var/lib/apt/lists/*

RUN curl -fsSL https://pyenv.run | bash
RUN export PYENV_ROOT="$HOME/.pyenv"
RUN [[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"
RUN eval "$(pyenv init - bash)"


CMD ["/bin/bash"]