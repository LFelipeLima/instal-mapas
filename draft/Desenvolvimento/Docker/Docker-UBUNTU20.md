```
edson@docker:~$ sudo -i
root@docker:~# apt update
root@docker:~# apt install git
root@docker:~# apt-get install apt-transport-https ca-certificates curl gnupg-agent software-properties-common
root@docker:~# curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -
root@docker:~# apt-key fingerprint 0EBFCD88
root@docker:~# add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable"
root@docker:~# apt-get update
root@docker:~# apt-get install docker-ce docker-ce-cli containerd.io
root@docker:~# exit
edson@docker:~$ sudo docker run hello-world
edson@docker:~$ sudo -i
root@docker:~# systemctl status docker
root@docker:~# apt install net-tools
root@docker:~# netstat -tunlp
root@docker:~# systemctl status docker
root@docker:~# exit
edson@docker:~$ sudo curl -L "https://github.com/docker/compose/releases/download/1.26.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
edson@docker:~$ sudo chmod +x /usr/local/bin/docker-compose
edson@docker:~$ which docker-compose
edson@docker:~$ ls -al /usr/local/bin/docker-compose
edson@docker:~$ sudo usermod -aG docker $(whoami)
edson@docker:~$ docker-compose --version
edson@docker:~$ git clone https://github.com/mapasculturais/mapasculturais-base-project.git mapa-JVE
edson@docker:~$ cd mapa-JVE/
edson@docker:~$ git remote set-url origin https://github.com/edsongs/mapa-JVE
edson@docker:~$ git push
edson@docker:~$ cd dev-scripts/
edson@docker:~$ sudo ./start-dev.sh

edson@docker:~$ docker-compose -f docker-compose.dev.yml build
edson@docker:~$ docker-compose -f docker-compose.dev.yml up
```