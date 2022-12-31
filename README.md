# Welcome to the Hyperpixel 4 & Raspberry Pi Mount for Voron 2.4 GitHub Repo

###### A quick disclaimer
*Please note that Print Up is not affiliated with Voron or the Voron Design Team. We are simply fans of the Voron printers and want to contribute to the open source community by providing helpful resources and support for these amazing machines.*

## About the Hyperpixel 4 Mount

The Hyperpixel 4 Mount for Voron 2.4 is a full solution for mounting the Hyperpixel 4 display by Pimoroni attached to a Raspberry Pi 3/4 via GPIO to a Voron 2.4 3D printer. This requires fully replacing the front skirt to your Voron 2.4 with a new bespoke solution that allows the almost vertical mounting of the Raspberry Pi directly behind the Hyperpixel Display.

The solution includes several 3D printable parts, a full visual manual, Hyperpixel configuration for Klipper Screen and more.

## Whats included in the repo?
- **STL files** - All the printed parts
- **STEP file** - Should you wish to modify or create your own varient
- **Install Manual** - For the printed parts
- **Hyperpixel Config Guide** - for Klipper Screen

# Hyperpixel Raspberry Pi Configuration

**Using Raspberry Pi OS Bullseye?**

Support for the Hyperpixel is built right into the OS, so no need to download anything! We just need to make some changes to the `/boot/config.txt` file as well as creating a new configuration for the screen rotation. 

**Not using Raspberry Pi OS Bullseye?**

If you're not using OS Bullseye then you will need to install the Hyperpixel using the instructions from Pimoroni. https://github.com/pimoroni/hyperpixel4

## Configuration 💻 ⬇️

> ❗️ Not installed the printed parts yet? We recommend installing those first, however, you can follow the configuration first if you want to test the screen before installing. 

> ❗️ Please note, this config method might not work for OS versions before Bullseye, but if it does, please let us know!

**1. Install Klipper Screen**

- If you haven't already, install Klipper Screen. We recommend following the Manual Install Guide here - https://klipperscreen.readthedocs.io/en/latest/Installation/#auto-install

**2. SSH into your Raspberry Pi**

- SSH into your Raspberry Pi using Terminal (MacOS/Linux) or PuTTY for Windows Users. In the example below just swap `yourpiaddress` for your Raspberry Pi's IP address or `yourpisname.local`

```
ssh pi@yourpiaddress
```

**3. Navigate to `/boot/config.txt` file**

- Using the following command, navigate to the `/boot/config.txt` file. 

```
sudo nano /boot/config.txt
``` 

**4. Add the following items to the config file**

- Add the following items to the bottom of your `config.txt` file

```
dtoverlay=vc4-kms-dpi-hyperpixel4

dtparam=rotate=90,touchscreen-swapped-x-y,touchscreen-inverted-y
```
**5. Save the changes**

- Save the changes to the `config.txt` file. 

**6. Now we nee

## How to get in contact with us

Should you have any questions, changes, or issues about this repo or you just want to say hi, drop us an email here - **info@printup.xyz**
