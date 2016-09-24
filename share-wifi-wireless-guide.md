#Sharing WiFi in Linux

This tutorial will walk you through on creating an AP to share internet, or not, creating a wireless network.
This method allows to share internet using only 1 interface (wlan) and creates a virtual interface on the machine, creating
a new network.

First, clone create_ap and install.

```
$ cd ~   
$ git clone https://github.com/oblique/create_ap
$ sudo apt-get install hostapd dnsmasq
$ cd create_ap
$ sudo make install
```

To run your WiFi network just do:
```
$ sudo create_ap <interface\> <interface\> <SSID\> <PASSWORD\>
Example: sudo create_ap wlan0 wlan0 lar \!zacarias.
```

If it doesn't work right away, try to specify a different driver for the wireless using --driver <DRIVER\>.

Finally, to specify a range of IP's, you should provide de gateway address.

```
$ sudo create_ap <interface\> <interface\> -g <gateway\> -d <SSID\> <PASSWORD\>
Example: sudo create_ap wlan0 wlan0 -g 172.16.49.254 -d lar \!zacarias.
```
More info on create_ap README.md

