# lorawan_battey_monitor_software
A docker compose script to accompany my lorawan battery monitor

https://github.com/matty0005/pico-LoRaWAN-battery-monitor

## Installation
Make sure you have the latest version of docker. If you are unsure if you have docker installed, you can check it is installed with the following command
```
docker -v
```
Assuming docker is installed, it should return a docker version number - you can skip the docker installation steps.

### Installing docker and docker-compose(Linux - Debian/Raspbian/Ubuntu)
#### Docker
First update any packages and lists
```
sudo apt-get update && sudo apt-get upgrade
```

Next download the docker install script using the following command
```
curl -fsSL https://get.docker.com -o get-docker.sh
```
Install it by executing the following
```
sudo sh get-docker.sh
```

Next add a non-root user to the docker group so that non-root users can run containers etc.
```
sudo usermod -aG docker ${USER}
```

#### Docker compose
To install docker compose, run the following commands - usually installed from pip.
```
sudo apt-get install libffi-dev libssl-dev
sudo apt install python3-dev -y
sudo apt-get install python3 python3-pip -y
sudo pip3 install docker-compose
```

Finally, you'll need to reboot your machine.

### Building and running containers
Once docker is installed, you'll need to clone this repository using the following.
```
git clone https://github.com/matty0005/lorawan_battey_monitor_software
```
After this, you can now change directory to the newly created folder 
```
cd lorawan_battey_monitor_software
```
Finally to start the containers you can run the following command
```
docker-compose up -d
```

Once the images are built, the container should now be running and give you the terminal back as we started the containers in detached mode.
