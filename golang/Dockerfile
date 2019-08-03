FROM golang:1.12.7

RUN apt update

RUN useradd -ms /bin/bash go-online

RUN echo "root:root" | chpasswd

ENTRYPOINT ["/main"]
RUN apt-get install -y zsh && apt-get install -y wget
RUN apt-get install -y git
USER go-online
RUN wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | sh
RUN export TERM=xterm && echo "unsetopt PROMPT_SP" >> ~/.zshrc

ENV LANG=C.UTF-8
