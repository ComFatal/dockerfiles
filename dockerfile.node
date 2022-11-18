FROM debian:buster-slim

RUN apt update && apt upgrade -y

RUN apt install nano openssh-server openssh-client net-tools iputils-ping python3 -y 

RUN sed -i 's/PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN sed -i 's/#PermitRootLogin/PermitRootLogin/' /etc/ssh/sshd_config
RUN sed -i 's#root:\*#root:sa3tHJ3/KuYvI#' /etc/shadow

RUN mkdir /run/sshd
ENTRYPOINT ["/usr/sbin/sshd"]
CMD ["-D"]
