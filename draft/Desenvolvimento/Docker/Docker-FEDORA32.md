```
*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*
Passo 1:
	[root@fedora ~]# yum update -y
    [root@fedora ~]# yum install git -y

*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*
Testar com a receita em https://fedoramagazine.org/docker-and-fedora-32/
*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*
Passo 2: (consultado https://computingforgeeks.com/how-to-install-docker-on-fedora/)
    [root@fedora ~]# dnf remove docker docker-client docker-client-latest docker-common docker-latest	\
                 	 docker-latest-logrotate docker-logrotate docker-selinux docker-engine-selinux docker-engine
    [root@fedora ~]# dnf -y install dnf-plugins-core
    [root@fedora ~]# tee /etc/yum.repos.d/docker-ce.repo<<EOF
[docker-ce-stable]
name=Docker CE Stable - \$basearch
baseurl=https://download.docker.com/linux/fedora/31/\$basearch/stable
enabled=1
gpgcheck=1
gpgkey=https://download.docker.com/linux/fedora/gpg
EOF
	[root@fedora ~]# dnf makecache
	[root@fedora ~]# dnf install docker-ce docker-ce-cli containerd.io
	[root@fedora ~]# systemctl enable docker
	[root@fedora ~]# dnf install docker-compose
	[root@fedora ~]# usermod -aG docker user	# opcional
	[root@fedora ~]# vi /etc/firewalld/firewalld.conf
FirewallBackend=iptables
	[root@fedora ~]# systemctl restart firewalld.service
	
*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*
Passo 3: (consultado site https://docs.docker.com/engine/install/fedora/)
	[root@fedora ~]# grubby --update-kernel=ALL --args="systemd.unified_cgroup_hierarchy=0"
	[root@fedora ~]# reboot

*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*
Passo 4:
	[user@fedora ~]$ sudo -i
	[sudo] senha para user:
	[root@fedora ~]# git clone https://github.com/mapasculturais/mapasculturais-base-project.git plataforma
	ou
	[root@fedora ~]# git clone https://github.com/mapasculturais/mapasculturais-aldirblanc plataforma
	[root@fedora ~]# cd ~/plataforma
	[root@fedora ~]# git remote set-url origin https://github.com/edsongs/plataforma
	[root@fedora ~]# git push
	[root@fedora ~]# cd dev-scripts
	[root@fedora ~]# ./start-dev-sh
```