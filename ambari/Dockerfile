FROM centos:latest

RUN yum install -y epel-release && yum update -y \
&& yum install -y initscripts systemd* yum-utils net-tools git curl unzip wget openssh-server openssh-clients \
java-1.8.0-openjdk java-1.8.0-openjdk-devel \
&& systemctl enable sshd \
&& yum clean all \
&& ssh-keygen -f /etc/ssh/ssh_host_rsa_key -t rsa -N ''

CMD ["/usr/sbin/sshd","-D"]

# Dockerfile
# Ambari
# docker build -t sxy/centos_ambari .
# docker run -itd --name m1 sxy/centos_ambari
# docker exec -it m1 /bin/bash