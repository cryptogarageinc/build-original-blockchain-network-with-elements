FROM ubuntu:18.04
WORKDIR /home/elements
RUN apt-get update && \
    apt-get install -y wget && \
    wget https://github.com/ElementsProject/elements/releases/download/elements-0.18.1.9/elements-0.18.1.9-x86_64-linux-gnu.tar.gz && \
    tar -zxvf elements-0.18.1.9-x86_64-linux-gnu.tar.gz && \
    install -m 0755 -o root -g root -t /usr/local/bin ./elements-0.18.1.9/bin/* && \
    rm -rf ./elements-0.18.1.9 \
    rm -f elements-0.18.1.9-x86_64-linux-gnu.tar.gz
ADD ./elements.conf /root/.elements/
CMD ["elementsd"]

