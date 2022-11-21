# 도커 안내서


## 0. 리눅스 머신 환경 준비
- AWS EC2 (Ubuntu) 인스턴스
- key pair, public IP 확인 후 접속

## 1. Docker 설치
```
$ curl -s https://get.docker.com/ | sudo sh
$ sudo usermod -aG docker ubuntu
```
- 설치 확인
```
$ docker version
Client: Docker Engine - Community
 Version:           20.10.21
 API version:       1.41
 Go version:        go1.18.7
 Git commit:        baeda1f
 Built:             Tue Oct 25 18:01:58 2022
 OS/Arch:           linux/amd64
 Context:           default
 Experimental:      true

Server: Docker Engine - Community
 Engine:
  Version:          20.10.21
  API version:      1.41 (minimum version 1.12)
  Go version:       go1.18.7
  Git commit:       3056208
  Built:            Tue Oct 25 17:59:49 2022
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          1.6.9
  GitCommit:        1c90a442489720eec95342e1789ee8a5e1b9536f
 runc:
  Version:          1.1.4
  GitCommit:        v1.1.4-0-g5fd4c4d
 docker-init:
  Version:          0.19.0
  GitCommit:        de40ad0

```

## 2. 컨테이너 만들기
```
ubuntu@ip-10-0-13-62:~$ docker run ubuntu:20.04
Unable to find image 'ubuntu:20.04' locally
20.04: Pulling from library/ubuntu
eaead16dc43b: Pull complete
Digest: sha256:450e066588f42ebe1551f3b1a535034b6aa46cd936fe7f2c6b0d72997ec61dbd
Status: Downloaded newer image for ubuntu:20.04
```
없으면 다운로드(pull)하여 생성 후 시작함

```
~ curl localhost:5678
hello world
```