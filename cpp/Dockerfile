FROM alpine:3
# 更改为华为源
RUN sed -i "s@http://dl-cdn.alpinelinux.org/@https://repo.huaweicloud.com/@g" /etc/apk/repositories && \
# 安装必备软件
    apk update && apk add --no-cache zsh git clang && \
# 添加运行时用户
    adduser -D go-online && echo "root:root" | chpasswd
# 添加zsh的配置
USER go-online
ADD install.sh install.sh
RUN cat install.sh | sh
ENV LANG=C.UTF-8 TERM=xterm
# 切回root用户
USER root
RUN rm install.sh
