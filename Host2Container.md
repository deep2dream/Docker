### [nginx](https://docs.docker.com/network/network-tutorial-host/)
    docker run --rm -d --network host --name my_nginx nginx
    ip addr show
    sudo netstat -tulpn | grep :80
    docker container stop my_nginx
