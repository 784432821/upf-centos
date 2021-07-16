FROM centos:7.6.1810

RUN yum install -y epel-release

RUN yum install -y pciutils \
    && yum install -y tcpdump \
    && yum install -y ethtool \
    && yum install -y hiredis-devel \
    && yum install -y net-tools \
    && yum install -y redhat-lsb \
    && yum install -y tcpreplay msgpack-devel \
    && yum install -y readline-devel libedit-devel \
    && yum install -y gcc automake autoconf libtool make \
    && yum install -y glibc-static libstdc++-static libevent-devel \
    && yum install -y iproute numactl mbedtls gdb numactl-devel numactl-libs \
    && yum install -y gnutls-devel \
    && yum install -y libmicrohttpd-devel \
    && yum install -y jansson-devel \
    && yum install -y systemd-devel \
    && yum install -y libcurl-devel \
    && yum install -y sysstat \
    && yum install -y perf \
    && yum -y install openssh-server

#修改/etc/ssh/sshd_config
#RUN sed -i 's/UsePAM yes/UsePAM no/g' /etc/ssh/sshd_config

# 生成sshkey
RUN ssh-keygen -t dsa -f /etc/ssh/ssh_host_dsa_key
RUN ssh-keygen -t rsa -f /etc/ssh/ssh_host_rsa_key

#变更root密码
#RUN echo "root:upf123!"|chpasswd

WORKDIR /opt/upu-5G
