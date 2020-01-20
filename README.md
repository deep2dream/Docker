### [Installation](https://github.com/gustavkkk/blockchain/blob/master/Exchange/Docker.md#install-ubuntu)
### [B@s!c Comm@nds](https://hub.docker.com)
    privilege
    sudo usermod -aG docker ${USER}

    initial
    ubuntu@ sudo docker pull ubuntu:16.04
    ubuntu@ sudo docker run --name waltchain-server -it ubuntu:16.04 bash
    root@ apt update
    root@ cd /
    root@ exit
    
    save image
    ubuntu$ sudo docker commit -m "Added WaltChain Server" -a "NAME" waltchain-server falcon/waltchain-server:latest
    
    run without save
    ubuntu@ sudo docker run -it frank/waltchain-server bash

    run with save
    ubuntu@ sudo docker start waltchain-server
    ubuntu@ sudo docker ps
    ubuntu@ sudo docker exec -it waltchain-server bash
    root@ cd /
    root@ exit
    ubuntu@ sudo docker stop waltchain-server
    ubuntu@ sudo docker ps

    export & import
    [container]
    ubuntu@ sudo docker ps -a
    ubuntu@ sudo docker export waltchain-server > waltchain-server.tar.gz
    ubuntu@ sudo docker export NAME | gzip > NAME.gz
    ubuntu@ sudo scp NAME.gz USERNAME@SERVER_IP:/home/USERNAME
    ubuntu@ sudo zcat NAME.gz | docker import - NAME
    ubuntu@ sudo docker run -i -t NAME /bin/bash
    [images]
    ubuntu@ sudo docker images
    ubuntu@ sudo docker commit 3a09b2588478 mynewimage 4d2eab1c0b9a13c83abd72b38e5d4b4315de3c9967165f78a7b817ca99bf191e
    ubuntu@ sudo docker save mynewimage > /tmp/mynewimage.tar
    ubuntu@ sudo docker load < /tmp/mynewimage.tar

    info
    ubuntu@ sudo docker ps
    ubuntu@ sudo docker container ls
    ubuntu@ sudo docker images
    
    remove image
    ubuntu@ sudo docker images
    ubuntu@ sudo docker rmi falcon/waltchain-server:version
    #  ubuntu@ sudo docker rmi image-id
    
    [COPY:host2guest,guest2host]
    ubuntu$ sudo docker cp abc.txt waltchain-server:/
    ubuntu$ sudo docker cp -a waltchain-server:/root/data /tmp
    
    [Access Hub/Upload Image]
    ubuntu$ sudo docker commit -m "Added WaltChain Server" -a "NAME" waltchain-server falcon/waltchain-server:latest
    ubuntu$ docker login
    ubuntu$ docker push falcon/waltchain-server
    ubuntu$ docker logout
### [Python3.6](http://ubuntuhandbook.org/index.php/2017/07/install-python-3-6-1-in-ubuntu-16-04-lts/)
    NEVER UNINSTALL PYTHON3.5. OR YOU WILL MAKE CHAOS.
    root@ apt install software-properties-common
    root@ add-apt-repository ppa:jonathonf/python-3.6
    root@ apt-get update
    root@ apt-get install python3.6
    root@ update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.5 1
    root@ update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.6 2
    
    root@ update-alternatives --config python3
    
    root@ rm /usr/bin/python3
    root@ ln -s python3.5 /usr/bin/python3
    
    root@ curl "https://bootstrap.pypa.io/get-pip.py" -o "get-pip.py" 
### [Install pkg$]()
    root@ apt update
    root@ apt install python python-pip vim net-tools
    root@ apt-get install -y iputils-ping
    root@ apt install git
    root@ apt install build-essential
    root@ apt install gcc
    root@ apt install python3.6-dev
    root@ apt-get install libssl-dev build-essential automake pkg-config libtool libffi-dev libgmp-dev libyaml-cpp-dev
    # root@ apt-get install build-essential autoconf libtool pkg-config python-opengl python-imaging python-pyrex python-pyside.qtopengl idle-python2.7 qt4-dev-tools qt4-designer libqtgui4 libqtcore4 libqt4-xml libqt4-test libqt4-script libqt4-network libqt4-dbus python-qt4 python-qt4-gl libgle3 python-dev
    root@ git clone https://github.com/ethereum/pyethereum
    root@ cd pyethereum
    root@ python3 setup.py install
        
    - truechain
    root@ git clone https://github.com/truechain/py-trueconsensus
    root@ cd py-trueconsensus
    root@ rm /usr/bin/python3
    root@ ln -s python3.5 /usr/bin/python3
    root@ apt-get install python3-setuptools
    root@ apt-get install protobuf-compiler
    root@ python3 setup.py install
    root@ pip3 install -r requirements.txt
    root@ cd trueconsensus
    root@ ./utils/generate_proto.sh
    root@ python3 -m utils.make_keys
    root@ python3 -m utils.generate_requests_dat
    root@ ./engine.py
    root@ ./client.py
    
    
