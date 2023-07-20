# authors: nanak <2152598815@qq.com>
# github <github.com/jiuyue112>
# update: 2023-07-20

#这个镜像使用ustc下载会更快
FROM nanak112/debian:ustc

MAINTAINER nanak (giehub.com/jiuyue1123)

RUN apt-get update -y \
&& apt-get install openssh-server python3 -y \
#必须创建这个目录否则无法启动ssh
&& mkdir -p /var/run/sshd \ 
#创建这个目录用来保存公钥
&& mkdir -p /root/.ssh 

ADD authorized_keys /root/.ssh/authorized_keys
ADD run.sh /run.sh
RUN chmod 755 /run.sh

CMD ["/run.sh"]

