FROM lambci/lambda:build-python3.7

RUN yum install -y zsh

ADD https://github.com/glsorre/dotfiles/archive/master.tar.gz /root

RUN tar -zxvf /root/master.tar.gz -C /root
RUN mv /root/dotfiles-master /root/.dotfiles
RUN ln -s /root/.dotfiles/zshrc /root/.zshrc

COPY init.sh /root/init.sh

RUN chmod 755 /root/init.sh

ENTRYPOINT  ["/root/init.sh"]
