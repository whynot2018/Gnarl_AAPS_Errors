# Gnarl_AAPS_Logs
Pump Medtronic 754 ver 2.6A 1.1<br>
AndroidAPS 2.7-omnipod-0.4-SNAPSHOT<br>
Build: EROS_0.2-342-g51fea....

Ubuntu 19
```
$ sudo apt-get remove docker docker-engine docker.io containerd runc
$ sudo apt-get install     apt-transport-https     ca-certificates     curl     gnupg-agent     software-properties-common
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
$ sudo apt-key fingerprint 0EBFCD88
$ sudo add-apt-repository    "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
$ sudo apt-get update
$ sudo apt-get install docker-ce docker-ce-cli containerd.ioapt-cache madison docker-ce
$ apt-cache madison docker-ce
$ sudo apt-get install docker-ce=5:19.03.8~3-0~ubuntu-eoan docker-ce-cli=5:19.03.8~3-0~ubuntu-eoan containerd.io
$ sudo docker run hello-world
$ sudo docker pull espressif/idf:release-v4.1
$ cd gnarl
$ rm -rf project
$ git pull
$ cd project/
$ lsusb
$ sudo docker run -it --rm -v $PWD:/project -w /project --device /dev/ttyUSB0 espressif/idf:release-v4.1
# idf.py build
# idf.py flash
# idf.py monitor
```
Ubuntu 20

sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
