FROM centos:8
ENV container docker
RUN yum -y install openssh-server; yum clean all; 
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
VOLUME [ "/sys/fs/cgroup" ]
RUN  /usr/bin/ssh-keygen -A; 
CMD ["/usr/sbin/sshd", "-D", "-e"]
#CMD ["/bin/bash"]
