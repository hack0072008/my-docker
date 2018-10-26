


# docker-ce 18.06.1 daemon.json
    {
        "insecure-registries": ["10.100.102.207:80", "10.100.102.208:80", "https://xxxx.dkr.ecr.cn-north-1.amazonaws.com.cn"],
        "dns": ["8.8.8.8", "8.8.4.4"],
        "data-root": "/mnt/data/docker_data",
        "storage-driver": "overlay2",
        "hosts": ["unix:///var/run/docker.sock", "tcp://0.0.0.0:2375"],                                                                                                                                                                                                           
        "debug": true
    }


# /etc/systemd/system/docker.service.d/https-proxy.conf
    [Service]
    Environment="NO_PROXY=localhost,127.0.0.1"

# /etc/systemd/system/docker.service.d/http-proxy.conf
    [Service]
    Environment="NO_PROXY=localhost,127.0.0.1"




~~完~~
