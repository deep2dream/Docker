### ENVIRONMENTAL VARIABLE[ubuntu@ vim ~/.bashrc]
    bftkeyhex1="e431e50943adc60ea07abcb7a03e0e86bbdb3ae5012849c78444d3145491d76a"
    bftkeyhex2="fa53cdcda2367d4f73b47ad54cb8bb69c9710ec1eee0e83eb09116e78feab969"
    bftkeyhex3="2dd9f2413286965fbba4d4d3424e0d1ca58827eca73f509272307dd83108ec48"
    bftkeyhex4="e05e13a43a0746824aabd5ba8e562efb279297df6bfd9fd369b0f74909a8116e"
    
    networkid=88 
    
    bootip='172.17.0.2'
    bftip1='172.17.0.3'
    bftip2='172.17.0.4'
    bftip3='172.17.0.5'
    bftip4='172.17.0.6'
### START BOOTNODE
    ubuntu@ sudo docker run --name truechain-dev -it falcon0125/truechain-dev:latest
    root@ truepub
    root@ truedel
    root@ mkdir $truedir
    root@ bootnodegen
    root@ bootnodestart
### ENVIRONMENTAL VARIABLE[ubuntu@ vim ~/.bashrc]
    truechain='/root/Code/github.com/truechain/truechain-engineering-code/build/bin'    bootnodedoc="enode://625004fc04124fc7306f784e360bb35e6567594fee14f2655e521c7c255a5b50a1ba74b671203e77b9778c4caf329d7727b5158f72f819dd48aeef7b97d15ca2@$bootip:30301"
    alias startcommittee1='sudo docker run --rm -it falcon0125/truechain-dev:latest bash -c "getrue console --networkid $networkid --bootnodes $bootnodedoc --election --bftkeyhex $bftkeyhex1 --bftip $bftip1"'
    alias startcommittee2='sudo docker run --rm -it falcon0125/truechain-dev:latest bash -c "getrue console --networkid $networkid --bootnodes $bootnodedoc --election --bftkeyhex $bftkeyhex2 --bftip $bftip2"'
    alias startcommittee3='sudo docker run --rm -it falcon0125/truechain-dev:latest bash -c "getrue console --networkid $networkid --bootnodes $bootnodedoc --election --bftkeyhex $bftkeyhex3 --bftip $bftip3"'
    alias startcommittee4='sudo docker run --rm -it falcon0125/truechain-dev:latest bash -c "getrue console --networkid $networkid --bootnodes $bootnodedoc --election --bftkeyhex $bftkeyhex4 --bftip $bftip4"'
    alias startminer='sudo docker run --rm -ti falcon0125/truechain-dev:latest bash -c "$truechain/getrue console --networkid $networkid --bootnodes $bootnodedoc"'
    
### START COMMITTEE
    startcommittee1
    startcommittee2
    startcommittee3
    startcommittee4
### START MINER
    startminer
    startminer
    startminer
    > personal.newAccount('1')
    > miner.start(1)
