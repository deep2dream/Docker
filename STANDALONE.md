### Q & A
    - Difference Between repository, image, container?
      > repository=image=vm
      > container is an instance. Multiple stances from one Image can be created.
    - 
# Distribute & RUN
### create containers
    $ ubunt@ sudo docker run --name waltchain-server -it falcon0125/waltchain-server:0.2
    $ ubunt@ sudo docker run --name waltchain-server-1 -it falcon0125/waltchain-server:0.2
    $ ubunt@ sudo docker run --name waltchain-server-2 -it falcon0125/waltchain-server:0.2
    $ ubunt@ sudo docker run --name waltchain-server-3 -it falcon0125/waltchain-server:0.2
    [default]
    any port is available over containers & host
    [expose]
    $ ubunt@ sudo docker run --expose=8000-65000/udp --expose=8000-65000/tcp --name waltchain-server -it falcon0125/waltchain-server:0.2
    [publish]
    $ ubunt@ sudo docker run -P --name waltchain-server -it falcon0125/waltchain-server:0.2
    $ ubunt@ sudo docker run -p 8000:65000 --name waltchain-server -it falcon0125/waltchain-server:0.2
### container2image
    $ sudo docker commit -m "error resolved" -a "NAME" waltchain-server falcon0125/waltchain-server:0.3
### run containers
    $ sudo docker start waltchain-server
    $ sudo docker start waltchain-server-1
    $ sudo docker start waltchain-server-2
    $ sudo docker start waltchain-server-3
    $ sudo docker exec -it waltchain-server bash
    $ sudo docker exec -it waltchain-server-1 bash
    $ sudo docker exec -it waltchain-server-2 bash
    $ sudo docker exec -it waltchain-server-3 bash
### attach
    $ docker attach waltchain-server
### remove containers
    $ sudo docker rm waltchain-server-x
### list
    - images
    $ sudo docker images
    - container
    all@ sudo docker container ls -a
    running@ sudo docker ps
### change name
    - tag, repo 
    $ sudo docker tag d583c3ac45fd falcon0125/waltchain-server:latest
    - container
    $ sudo docker rename truechain truechain-server
