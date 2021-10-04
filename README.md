# rtl-ais-tcz
rtl_ais extension for piCore

Get depending rtl-sdr package from piCore 7.x:
http://distro.ibiblio.org/tinycorelinux/7.x/armv6/tcz/

echo "/usr/local/bin/rtl_ais -T -p 35 -g 20" >> /opt/bootlocal.sh
filetool.sh -b

or use for hotplugging an udev rule eg. 99-rtl-sdr.rules (vendor and product id must reflect your device): 
SUBSYSTEM=="usb", ATTRS{idVendor}=="0bda", ATTRS{idProduct}=="2838", RUN+="/usr/local/bin/rtl_ais -T -g 30"

add /etc/udev/rules.d/99-rtl-sdr.rule to /opt/.filetool.lst to enable backup for the rule and backup with filetool.sh -b
