### CENTOS7
     hostnamectl
     yum check-update
     yum install curl
     curl -fsSL https://get.docker.com/ | sh
     yum install yum-utils device-mapper-persistent-data lvm2
     yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
     yum install docker-ce
     systemctl start docker
     systemctl enable docker
     docker -v
