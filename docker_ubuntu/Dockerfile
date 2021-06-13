FROM ubuntu:20.04
ENV container docker
RUN export DEBIAN_FRONTEND=noninteractive;\
ln -fs /usr/share/zoneinfo/Europe/Moscow /etc/localtime; \
apt-get update;\
apt-get install -y tzdata;\
dpkg-reconfigure --frontend noninteractive tzdata;\
apt-get install -y openssh-server;\
apt-get clean; \
mkdir /run/sshd; \
chmod 755 /run/sshd; \
rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN mkdir -p /root/.ssh; echo \
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDBmXO0y0NB1Tn1atO1\
Jx8ne1l9N6IVBi7qFHrfVZ+Xcox7DxwFUOBSPpkj2xmDSdqotkCpTAed\
tEx8FBdkhX63bbucvMfnxFR3+5ZCHo7NFGnldVMMqsE6yPxpfqNfwe3D\
txTMrWL2un5jnihygSkY+QMEbYadpzOJIGe/UrhdtzDK/rlTGeUsl5d3\
0EDQMp8vcRZLwhvGaPtCo1PHJ2iVniLr00C8D+JgnqDqitzz8Gwsiuxn\
IHByzGkskVBDAldub9h08eTrodfu+7+TiVlupREbQ0RFoj8e/0cpX/PX\
RIzyWAypiNEUHNnr/yx4w3KbNccn5NjS5y4uKwZAsybSSgX2W7b5QJ0u\
KKhXbOOXcgAjY8igCGjeUVSKTJ9KStMpenfNBV+1S/YwaSgJeImNtGdC\
0si72E4FSQW76PSWn4xmzVXmV2BGC2mZ3w0s6sOeg+W7STVxczJcvHPN\
IqZESq1q4agKHaYFSoi7gTJzRdcBMawwe1ckg3ek4E6x31E= root@centos \
>> /root/.ssh/authorized_keys; \
chmod -R go= /root/.ssh;
CMD ["/usr/sbin/sshd", "-D", "-e"]
