
 
# 1.docker安装(1.10.0+)
    2.a yum install -y yum-utils device-mapper-persistent-data lvm2
    2.b yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
    2.c yum install docker-ce  or   yum list docker-ce --showduplicates | sort -r
        yum install docker-ce-<VERSION STRING>
    2.d systemctl start docker
        systemctl stop docker
    2.e 修改docker仓库目录：
        touch /etc/docker/daemon.json 
        cat /etc/docker/daemon.json:
        {
            "graph": "/data1/docker-data"
        }
        重启docker服务：
        systemctl restart docker
    
# 2.docker-compose安装(1.7.1+)
    3.a curl -L "https://github.com/docker/compose/releases/download/1.22.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
        chmod +x /usr/local/bin/docker-compose
        docker-compose --version

# 3.harbor安装(latest v1.5.3)
    1.a 在线安装
    1.b 离线安装
        --源码安装
        --二进制文件安装
    1.c wget https://storage.googleapis.com/harbor-releases/harbor-offline-installer-v1.5.3.tgz
        tar zxvf harbor-offline-installer-v1.5.3.tgz
        cd harbor
        vim /etc/harbor.cfg, 修改 hostname 为本机ip地址
        ./install.sh

# 4.名词解释
    4.a notary
        https://github.com/docker/notary
        是一套docker镜像的签名工具, 用来保证镜像在pull,push和传输工程中的一致性和完整性。
    4.b Docker-Compose
        https://github.com/docker/compose
        Docker-Compose 是 Docker 容器进行编排的工具，定义和运行多容器的应用，可以一条命令启动多个容器，使用Docker Compose不再需要使用shell脚本来启动容器。
    
    
    
    
    
    
    
    
    
