# insta2twislack4pi02🐢
This document is a guide for installing [insta2twislack](https://github.com/tmatsumor/insta2twislack) on an Raspberry Pi Zero 2 W.

## 1. Pre-installation

### 1.1. Install Raspberry Pi OS to a microSD card 
- Visit the [Download page](https://www.raspberrypi.com/software/) and install Raspberry Pi OS to your microSD card storage. 


<details>
<summary>More detail</summary>

## 1.1.1. Device, OS, and Storage
- Select "Raspberry Pi Zero2 W" device and your microSD card.

![image](https://github.com/tmatsumor/insta2twislack4pi02/assets/129941863/5fe085e0-c9e0-4b5b-8de4-491f5f8f3cf7)

- Click "Raspberry Pi OS (other)" and select "Raspberry Pi OS Lite(64-bit)".

![image](https://github.com/tmatsumor/insta2twislack4pi02/assets/129941863/1831ed0f-632b-4204-b680-5e4a95e14a20)

# 1.1.2. OS customization settings

- Click Next button.
- Then click EDIT SETTING button.

![image](https://github.com/tmatsumor/insta2twislack4pi02/assets/129941863/d9bf3f33-8671-4dcd-a5e0-b5fd1da24802)

- You can preconfigure the username and password, Wi-Fi settings.

![image](https://github.com/tmatsumor/insta2twislack4pi02/assets/129941863/67a8427e-9694-4711-bbd7-d845ac463ba4)

- Click "SERVICES" Tab.
- Click "Allow public-key authentication only" radio button.
- Click "RUN SSH-KEYGEN" button. 

![image](https://github.com/tmatsumor/insta2twislack4pi02/assets/129941863/441217b8-fdf2-49e8-a1e0-0d6e5b3fd7e2)

### 1.1.3. Write
- Click "SAVE" button on the OS Customisation dialog.
- Click "YES" button on the Use OS Customisation dialog.
- The writing process will begin.

![image](https://github.com/tmatsumor/insta2twislack4pi02/assets/129941863/3cff1173-aa4a-477b-afdb-047de6569f48)
</details>

### 1.2. Disable ipv6
Disable ipv6 to avoid mDNS related problems.
<details>
<summary>More detail</summary>
  
### 1.2.1. Open cmdline.txt file
  
- Eject the microSD card from your computer.
- Inject the sd card again.
- Open cmdline.txt file.
  
![image](https://github.com/tmatsumor/insta2twislack4pi02/assets/129941863/eee3790b-dc95-497c-83b7-cf11037ee74a)

### 1.2.2. Append "ipv6.disable=1" 

- Append "ipv6.disable=1" to the end of the line with a white space separator.
- Save the file.

![image](https://github.com/tmatsumor/insta2twislack4pi02/assets/129941863/218774fd-2507-49e3-8322-4ad423fbdadb)

</details>

### 1.3. Boot Pi Zero 2 W
- Insert the microSD card into your Raspberry Pi Zero 2 W and boot.

### 1.4. Install git, php and php-curl
- Connect to your Pi zero with SSH and install git, php and php-curl.
<details>
<summary>More detail</summary>

### 1.4.1. Connect to your Pi zero with SSH

- Open Power Shell on Windows and type the command below.
```
ssh _username_@raspberrypi.local
```

### 1.4.2. install git, php and php-curl

- Type the command below.

```
sudo apt-get update
sudo apt-get upgrade -y
sudo apt-get install -y git
sudo apt-get install -y php
sudo apt-get install -y php-curl
```
</details>

## 2. Setup insta2twislack

## 2.1. Install insta2twislack

- See this ["Installation" section](https://github.com/tmatsumor/insta2twislack).

## 2.2. Test insta2twislack

- See this ["Example" section](https://github.com/tmatsumor/insta2twislack).

## 2.3. Add jobs to crontab

- Add a job to run insta2twislack every three minutes.
- Add a job to reboot your pi zero at three am every day.

<details>
<summary>More detail</summary>

- Type the command below.

```
sudo cp /etc/crontab /etc/cron.d/insta2twislack
sudo echo "*/3 * * * * root (cd /home/tmatsumor/insta2twislack && sudo php insta2twislack.php)" | sudo tee -a /etc/cron.d/insta2twislack > /dev/null
sudo echo "0 3 * * * root sudo /sbin/reboot" | sudo tee -a /etc/cron.d/insta2twislack > /dev/null
sudo service cron restart
```
</details>


