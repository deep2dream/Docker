### [enable host](https://docs.docker.com/network/network-tutorial-host/)
    docker run --rm -d --network host --name my_nginx nginx
    ip addr show
    sudo netstat -tulpn | grep :80
    docker container stop my_nginx
### open port
    - [127.0.0.1 > 0.0.0.0](https://serverfault.com/questions/78048/whats-the-difference-between-ip-address-0-0-0-0-and-127-0-0-1)
    owt --rpc
    - [centos](https://stackoverflow.com/questions/19034542/how-to-open-port-in-centos)
    systemctl status firewalld -l
    systemctl enable firewalld
    systemctl start firewalld
    firewall-cmd --zone=public --permanent --add-port=8000/tcp
    firewall-cmd --reload
