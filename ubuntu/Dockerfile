FROM ubuntu

RUN apt update && apt install -y git

RUN echo "root:root" | chpasswd

ENTRYPOINT ["/main"]

ENV LANG=C.UTF-8
