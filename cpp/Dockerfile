FROM ubuntu

RUN apt update && apt install -y g++ gdb git

RUN echo "root:root" | chpasswd

ENTRYPOINT ["/main"]

ENV LANG=C.UTF-8
