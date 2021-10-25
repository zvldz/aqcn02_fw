# Modifying Aqara Hub E1(aqcn02/ZHWG16LM) firmware via telnet
Telnet must be opened on the hub via php-miio/python-miio(https://gist.github.com/zvldz/1bd6b21539f84339c218f9427e022709#aqara-hub-e1-zhwg16lm-usb-stick).
You will need telnet client like putty or other.
You can find out IP of the hub in MiHome or on your router.
Login - "root", no password.

<img src="../media/e1_screen_1.png" width="400">

<img src="../media/e1_screen_2.png" width="400">

## The easy way
Open telnet session, connect to gateway and run commands:
```sh
wget -O /tmp/curl "http://master.dl.sourceforge.net/project/aqcn02/bin/curl?viasf=1" && chmod +x /tmp/curl
/tmp/curl -s -k -L -o /tmp/update.tgz https://raw.githubusercontent.com/zvldz/aqcn02_fw/main/update/aqara_e1_files.tgz
tar -C / -xzf /tmp/update.tgz && source /data/profile
```

<img src="../media/e1_screen_3.png" width="400">

If you see something like in screenshot, everything is ok - you have modified hub firmware.

