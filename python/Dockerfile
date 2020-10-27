FROM python:2

RUN apt update && useradd -ms /bin/bash go-online && echo "root:root" | chpasswd && \
    apt-get install -y zsh wget git

USER go-online
RUN wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | sh && \
    export TERM=xterm
RUN pip install -i https://pypi.tuna.tsinghua.edu.cn/simple python-language-server pycodestyle autopep8 pyflakes yapf pydocstyle pylint mccabe rope

USER root

ENTRYPOINT ["/main"]

ENV LANG=C.UTF-8
ENV TERM=xterm
