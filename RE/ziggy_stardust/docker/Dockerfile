from debian as base

WORKDIR /root/

RUN apt update -y
RUN apt upgrade -y
RUN apt update -y



RUN apt install -y qemu-user socat gcc-12-riscv64-linux-gnu --fix-missing

WORKDIR "/root/"

COPY chal .
COPY flag.txt .

#USER nobody

EXPOSE 5000

ENTRYPOINT ["socat", "-dd", "TCP4-LISTEN:5000,fork,reuseaddr", "EXEC:\"qemu-riscv64 -L /usr/riscv64-linux-gnu/ chal\",pty,echo=0,raw,iexten=0"]

