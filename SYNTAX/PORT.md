### OPEN/CLOSE CHECK
    ubuntu@ sudo docker attach containerid
    root@ apt install nmap
    root@ nmap -p 30310 localhost
    root@ netstat -lntup
### OPEN PORT
    root@ apt install ufw
    root@ apt-get install linux-image-$(uname -r)
### DOCKER
    ubuntu@ sudo docker inspect container-name
    ubuntu@ sudo docker port container-name
    ubuntu@ sudo docker run --name waltchain-server-1 -it falcon0125/waltchain-server:0.2
    ubuntu@ sudo docker ps -a
### [EXPOSE & PUBLISH](https://stackoverflow.com/questions/22111060/what-is-the-difference-between-expose-and-publish-in-docker)
    3 OPTIONS
    - NO EXPOSE, NO PUBLISH: only accessible from inside the container itself
    - EXPOSE: inter-container communication
    - EXPOSE & PUBLISH: accessible from anywhere, even outside Docker
### TCP & UDP
    DEFAULT: TCP
    $ docker run -p 80:80/tcp -p 80:80/udp
### TRUECHAIN PORT
    30310, 30311, 30313, 30303, 30411, 52610
    
