# Add Docker's official GPG key:
```  
sudo apt-get update
```  
```  
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc
# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```  
```  
sudo apt-get update
```
```  
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```  
```  
xhost +
```  
```  
docker image pull ubuntu:20.04
```  
```  
docker run -tid --privileged -v /dev/bus/usb:/dev/bus/usb -v /tmp/.X11-unix:/tmp/.X11-unix:ro -v $XAUTHORITY:/home/user/.Xauthority:ro --net=host --env="DISPLAY=$DISPLAY" --env="LC_ALL=C.UTF-8" --env="LANG=C.UTF-8" --name wifieviltwin ubuntu:20.04
```  
```  
docker exec -ti wifieviltwin /bin/bash
```  
```  
apt update
```  
```  
apt install nano wireshark
```  
```  
apt install net-tools
```  
```  
apt install wireshark
```  
```  
apt install tcpdump 
```  
```  
apt install bridge-utils
```  
```  
apt install hostapd dnsmasq
```  
```  
apt install make git
```  
```  
apt install iproute2
```  
```  
apt install mousepad
```  
```  
apt install gedit
```  
For my connexion internet : wlp3s0 </br>
For sharing internet : wlx001c50b41782 </br>
</br>
first parameter of create_ap is the wifi interface </br>
second parameter of create_ap is the internet interface </br>
third parameter of create_ap is the name of acces point </br>
fourth parameter of create_ap is </br>
```  
docker exec -ti wifieviltwin bash create_ap/create_ap wlx001c50b41782 wlp3s0 MyAccessPoint
```
```  
docker ps
```  
For having <id>
```  
docker commit id wifieviltwin
```  
```  
docker save wifieviltwin -o wifieviltwin.tar.gz
```  
# LOAD AND RUN
```  
docker load -i  wifieviltwin.tar.gz
```  
```  
docker run -tid --privileged -v /dev/bus/usb:/dev/bus/usb -v /tmp/.X11-unix:/tmp/.X11-unix:ro -v $XAUTHORITY:/home/user/.Xauthority:ro --net=host --env="DISPLAY=$DISPLAY" --env="LC_ALL=C.UTF-8" --env="LANG=C.UTF-8" --name wifieviltwin ubuntu:20.04
```  
```  
docker exec -ti wifieviltwin bash create_ap/create_ap wlx001c50b41782 wlp3s0 MyAccessPoint
```
