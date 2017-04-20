# wink2
Version 2 of the fabulous Winkenthith controller, now 100% running on the BeagleBone

# Config Wifi

`nano /etc/network/interfaces`

```
allow-hotplug wlan1
iface wlan1 inet dhcp
    wpa-conf /etc/wpa_supplicant/wpa_supplicant.conf
```


```
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1

network={
    ssid="MarcottFreeISP-fios"
    key_mgmt=WPA-PSK
    psk="this is secret"
}
```
