# Installing OpenBMC on Ubuntu 24.04 LTS x64 Cloud Server

This guide provides detailed instructions for installing OpenBMC on an Ubuntu 24.04 LTS (64-bit) cloud server.

## Prerequisites
- Access to an Ubuntu 24.04 LTS x64 cloud server instance
- Basic knowledge of Linux command line

## Step 1: Install Required Packages
1. Update the package list:
   ```bash
   sudo apt update

2. Install the required packages:
   ```bash
   sudo apt install -y git build-essential fakeroot debhelper \
   libssl-dev libyaml-dev python3-pip python3-setuptools python3-wheel \
   libglib2.0-dev libfdt-dev libpixman-1-dev zlib1g-dev libarchive-dev

## Step 2: Clone OpenBMC Repository
  ```bash 
  git clone https://github.com/openbmc/openbmc.git

**## Step 3: Build OpenMBC**
  ```bash
  cd openbmc

## Step 4: Flash OpenBMC Image
1. Flash the OpenBMC image to a USB drive:
  ```bash
  sudo dd if=tmp/deploy/images/am57xx-evm/obmc-phosphor-image-am57xx-evm.wic of=/dev/sdX bs=4M conv=fsync
Replace /dev/sdX with the appropriate device name for your USB drive.

## Step 5: Boot OpenBMC
Insert the USB drive into the target machine.
Boot the machine from the USB drive to start OpenBMC.

## Step 6: Access OpenBMC Web Interface
Open a web browser and enter the IP address of your OpenBMC machine.
Log in with the default credentials (username: root, password: 0penBmc).

## Step 7: Configure OpenBMC
Follow the on-screen instructions to configure OpenBMC for your environment.
Congratulations! You have successfully installed and configured OpenBMC on your Ubuntu 24.04 LTS x64 cloud server.
