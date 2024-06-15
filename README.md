# insta2twislack4pi02🐢
This document is a guide for installing [insta2twislack](https://github.com/tmatsumor/insta2twislack) on an Raspberry Pi Zero 2 W.

## 1. Pre-installation

### 1.1. Install Raspberry Pi OS to a microSD card 
- Visit the [Download page](https://www.raspberrypi.com/software/) and install Raspberry Pi OS to your microSD card. 

- More details

### 1.2. Boot Pi Zero 2 W
- Insert the microSD card into your Raspberry Pi Zero 2 W and boot.

- More details

### 1.3. Install git, php and php-curl
- Connect your Pi zero by ssh and type the commands below.
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install -y git
sudo apt-get install php -y
sudo apt-get install php-curl -y
```

