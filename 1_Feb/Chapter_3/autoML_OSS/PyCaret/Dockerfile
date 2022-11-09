FROM ubuntu:20.04
USER root

# Python Version
ENV PYTHON_VERSION 3.7.10
#ENV PYTHON_VERSION 3.10.7

ENV HOME /root
ENV PYTHON_ROOT $HOME/local/python-$PYTHON_VERSION
ENV PATH $PYTHON_ROOT/bin:$PATH
ENV PYENV_ROOT $HOME/.pyenv
ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get upgrade -y

# Install Node.js
RUN apt-get install -y --no-install-recommends curl
RUN curl -sL https://deb.nodesource.com/setup_12.x |bash - \
    && apt-get install -y nodejs

RUN apt-get install -y \
       wget \
       git \
       nano \
       vim \
       make \
       cmake \
       build-essential \
       libssl-dev \
       zlib1g-dev \
       libbz2-dev \
       libreadline-dev \
       libsqlite3-dev \
       llvm \
       libncurses5-dev \
       libncursesw5-dev \
       xz-utils \
       tk-dev \
       libffi-dev \
       liblzma-dev \
       libgomp1 \
    && git clone https://github.com/pyenv/pyenv.git $PYENV_ROOT \
    && $PYENV_ROOT/plugins/python-build/install.sh \
    && /usr/local/bin/python-build -v $PYTHON_VERSION $PYTHON_ROOT

## mecab
##https://system.blog.uuum.jp/entry/2019/10/18/110000
#RUN apt-get install -y \
#        mecab \
#        libmecab-dev \
#        mecab-ipadic \
#        mecab-ipadic-utf8
#RUN git clone --depth 1 https://github.com/neologd/mecab-ipadic-neologd.git \
#    && cd mecab-ipadic-neologd \
#    && bin/install-mecab-ipadic-neologd -n -y
#RUN pip3 install mecab-python3

#RUN apt-get autoremove -y \
#    && apt-get clean \
#    && rm -rf \
#        $PYENV_ROOT \
#        /var/lib/apt/lits/*

# install python library
#COPY requirements.txt ./
RUN pip3 install --upgrade pip && \
    #pip3 install --no-cache-dir -r requirements.txt \
    #&& rm -rf ~/.cache/pip
    rm -rf ~/.cache/pip

# set a theme for jupyterthemes
#RUN jt -t chesterish -T -N

# install jupyterlab & extentions
RUN pip3 install --upgrade --no-cache-dir \
    autopep8 \
    jupyterlab \
    #'jupyterlab~=3.0' \
    #'jupyterlab-kite>=2.0.2' \
    jupyterlab_code_formatter \
    jupyterlab-vimrc \
    yapf \
    && rm -rf ~/.cache/pip && \
    jupyter notebook --generate-config
#RUN jupyter lab build --dev-build=False --minimize=False
#RUN jupyter labextension install \
#        @hokyjack/jupyterlab-monokai-plus \
#        @ryantam626/jupyterlab_code_formatter \
#        @jupyterlab/toc \
#        @axlair/jupyterlab_vim \
#        @lckr/jupyterlab_variableinspector \
#        @jupyter-widgets/jupyterlab-manager \
#    && jupyter serverextension enable --py jupyterlab_code_formatter

## install jupyter-kite
#RUN cd && \
#    wget https://linux.kite.com/dls/linux/current && \
#    chmod 777 current && \
#    sed -i 's/"--no-launch"//g' current > /dev/null && \
#    ./current --install ./kite-installer

WORKDIR /home

RUN echo 'c.NotebookApp.token = "ShellScriptMagAutoML"' >> jupyter_notebook_config.py

#RUN mkdir /work
#WORKDIR /work

RUN pip3 install pycaret