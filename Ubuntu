## RTL8188EE
My Ubuntu with Wireless was unpredictable and slow. 
It seems to be a bug those hardware modules have MSI compatibility issue, so you could try to toggle its module parameter "msi".
```bash
sudo -i
echo "options rtl8188ee msi=1"  >  /etc/modprobe.d/rtl8188ee.conf
exit
```
