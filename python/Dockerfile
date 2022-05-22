FROM linuxserver/code-server
RUN sudo apt-get update
RUN sudo apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev \
    libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \
    xz-utils tk-dev
ENV HOME="/config"
ENV PYTHON_VERSION=3.7.6
ENV SKELETON_CODE /home/skeleton/pa2.c
WORKDIR $HOME

RUN git clone https://github.com/pyenv/pyenv.git .pyenv

ENV PYENV_ROOT="$HOME/.pyenv"
ENV PATH="$PYENV_ROOT/shims:$PYENV_ROOT/bin:$PATH"

RUN pyenv install ${PYTHON_VERSION}
RUN pyenv global ${PYTHON_VERSION}

COPY ${SKELETON_CODE} /config
