# wink2
Version 2 of the fabulous Winkenthith controller, now 100% running on the BeagleBone

# Config Wifi

`nano /etc/network/interfaces`

```
allow-hotplug wlan1
iface wlan1 inet dhcp
    wpa-conf /etc/wpa_supplicant/wpa_supplicant.conf
```

`nano /etc/wpa_supplicant/wpa_supplicant.conf`

```
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1

network={
    ssid="MarcottFreeISP-fios"
    key_mgmt=WPA-PSK
    psk="this is secret"
}
```

# remote access

## Weaved

```
sudo apt-get update
```
Then follow these...

https://github.com/weaved/installer/tree/master/Raspbian%20deb/1.3-03

Shows up on old developer portal

## Dataplicity

Also needs a `pt-get update`first

# install software

```
git clone https://github.com/bigjosh/wink2`
cd wink2
cp ledscape-config.json /etc/
./install.sh
./install-service.sh
```




