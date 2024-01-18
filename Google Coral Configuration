# Setting up Google Coral on Raspberry Pi

## 1. Install the Edge TPU runtime

1. Add the Debian package repository to the Raspberry:
echo "deb https://packages.cloud.google.com/apt coral-edgetpu-stable main" | sudo tee /etc/apt/sources.list.d/coral-edgetpu.list

curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -

sudo apt-get update

2. Install the Edge TPU runtime:
sudo apt-get install libedgetpu1-std

3. Now connect the USB Accelerator to your computer using the provided USB 3.0 cable.

## 2. Install the PyCoral library

sudo apt-get install python3-pycoral
