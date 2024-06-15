# insta2twislack4pi02🐢
This document is a guide for installing [insta2twislack](https://github.com/tmatsumor/insta2twislack) on an Raspberry Pi Zero 2 W.

## 1. Pre-installation

### 1.1. Install Raspberry Pi OS to a microSD card 
- Visit the [Download page](https://www.raspberrypi.com/software/) and install Raspberry Pi OS to your microSD card. 


<details>
<summary>More detail</summary>

## 1.1.1. Device, OS, and Storage
- Select "Raspberry Pi Zero2 W" device and your microSD card.

![image](https://github.com/tmatsumor/insta2twislack4pi02/assets/129941863/5fe085e0-c9e0-4b5b-8de4-491f5f8f3cf7)

- Click "Raspberry Pi OS (other)" and select "Raspberry Pi OS Lite(64-bit)".

![image](https://github.com/tmatsumor/insta2twislack4pi02/assets/129941863/1831ed0f-632b-4204-b680-5e4a95e14a20)

# 1.1.2. OS customization settings


![image](https://github.com/tmatsumor/insta2twislack4pi02/assets/129941863/d9bf3f33-8671-4dcd-a5e0-b5fd1da24802)

![image](https://github.com/tmatsumor/insta2twislack4pi02/assets/129941863/67a8427e-9694-4711-bbd7-d845ac463ba4)

</details>

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

