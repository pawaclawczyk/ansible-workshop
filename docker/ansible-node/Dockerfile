FROM debian:8

RUN apt-get update && apt-get install -y \
    openssh-server \
    python \
    vim \
    --no-install-recommends && rm -r /var/lib/apt/lists/*

RUN mkdir /var/run/sshd

RUN mkdir /root/.ssh

ADD authorized_keys /root/.ssh/authorized_keys

EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]
