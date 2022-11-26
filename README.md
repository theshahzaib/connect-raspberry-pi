# connect raspberry pi
 Connect Raspberry Pi without Screen Required

## 1. Connect Raspberry Pi with Wifi without Monitor

Create a file named `wpa_supplicant.conf` in the boot partition of the SD card, and add the following content:

```shell
    country=US
    ctrl_interface=DIR=/var/run/wpa_supplicant
    update_config=1

    network={
        ssid="your_wifi_name"
        psk="your_wifi_password"
        priority=1
    }

    network={
        ssid="your_wifi_name"
        psk="your_wifi_password"
        priority=2
    }
```

Replace `your_wifi_name` and `your_wifi_password` with your own wifi name and password.


    

## 2. Connect Raspberry Pi with Ethernet without Monitor

Create a file named `ssh` in the boot partition of the SD card, remain it empty.

## 3. Connect Raspberry Pi with Remote Desktop

### 3.1 Install xrdp

```shell
sudo apt-get install xrdp
```

### 3.2 Go to `Remote Desktop Connection` on Windows

Enter the `IP address` of the Raspberry Pi or type `raspberrypi` , and click `Connect`.

### 3.3 Login

The default username is `pi` and the default password is `raspberry`.

## 4. Connect Raspberry Pi with VNC

### 4.1 Install VNC Server

```shell
sudo apt-get install realvnc-vnc-server realvnc-vnc-viewer
```

### 4.2 Start VNC Server

```shell
vncserver
```

### 4.3 Connect Raspberry Pi with VNC Viewer

Enter the `IP address` of the Raspberry Pi or type `raspberrypi` , and click `Connect`.

### 4.4 Login

The default username is `pi` and the default password is `raspberry`.






