FROM python:2

RUN apt update && apt install -y git

RUN echo "root:root" | chpasswd

RUN pip install -i https://pypi.tuna.tsinghua.edu.cn/simple python-language-server pycodestyle autopep8 pyflakes yapf pydocstyle pylint mccabe rope

ENTRYPOINT ["/main"]

ENV LANG=C.UTF-8
