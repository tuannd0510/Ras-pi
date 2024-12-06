Step 1: Create a file name "wpa_supplicant.conf" with content:
```
country=us
update_config=1
ctrl_interface=/var/run/wpa_supplicant

network={
 scan_ssid=1
 ssid="ten wifi"
 psk="mat khau"
}
```
Step 2: Copy file tren vao thu muc chua cac file sau:
```
bootcode.bin
loader.bin
start.elf
kernel.img
cmdline.txt
```
