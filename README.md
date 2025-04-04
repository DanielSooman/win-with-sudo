# win-with-sudo
Windows on terminal (w/ sudo)

```
sudo su
```
```
sudo apt update
```
```
sudo apt install docker.io docker-compose
```
```
pwd
```
```
mkdir dockercom
```
```
cd dockercom
```

```
nano windows10.yml
```
### Now, Paste following in the yml file
```
services:
  windows:
    image: dockurr/windows
    container_name: windows
    environment:
      VERSION: "10"
      USERNAME: "SOURAV SEC"
      PASSWORD: "admin@123"
      RAM_SIZE: "4G"
      CPU_CORES: "4"
      DISK_SIZE: "400G"
      DISK2_SIZE: "100G"
    devices:
/dev/kvm
/dev/net/tun
    cap_add:
NET_ADMIN
    ports:
"8006:8006"
"3389:3389/tcp"
"3389:3389/udp"
    stop_grace_period: 2m
```
```
cat windows10.yml
```
```
sudo docker-compose -f windows10.yml up
```

Now view port! 
