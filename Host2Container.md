### [nginx](https://docs.docker.com/network/network-tutorial-host/)
    docker run --rm -d --network host --name my_nginx nginx
    ip addr show
    sudo netstat -tulpn | grep :80
    docker container stop my_nginx
### [open port](https://stackoverflow.com/questions/19034542/how-to-open-port-in-centos)
    systemctl enable
    systemctl start
    firewall-cmd --zone=public --permanent --add-port=8000/tcp
    firewall-cmd --reload
