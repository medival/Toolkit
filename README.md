# My Essentials Tools for Working

- Winbox
- Mikrotik Voucher Generator
- Ubiquiti Firmware (XM, XW)
- Ubnt Discovery

### Here how to show compliance test in ubnt radio

*This only works on ubnt firmware < v6.1.6*

1. Set your ip 192.168.1.x
2. Open ssh with [putty](https://the.earth.li/~sgtatham/putty/latest/w32/putty-0.74-installer.msi) or using Terminal if using linux
3. Set user **ubnt** and default ip address is **192.168.1.20**
4. Then show prompt, click yes
5. type your password. default is **ubnt**
6. then type `touch /etc/persistent/ct`
7. save your config using command `save`
8. Reboot your ubnt devices `reboot`
9. Login to your ubnt devices
10. There should be Compliance Test in your country
