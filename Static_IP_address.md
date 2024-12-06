Edit file /etc/dhcpcd.conf
```shell
sudo nano /etc/dhcpcd.conf
```

Content
```
interface eth0

static ip_address=192.168.0.10/24
static routers=192.168.0.1
static domain_name_servers=8.8.8.8 208.67.222.222

interface wlan0

static ip_address=192.168.0.200/24
static routers=192.168.0.1
static domain_name_servers=8.8.8.8 208.67.222.222
```

# Cac tham so
|Params|Des|
|--------------|--------------|
|**interface**|Định dang card mạng bạn muốn sử dụng, như ở trên chúng tôi có nói là mạng dây hoặc Wifi|
|--------------|--------------|
|**static ip_address** | Địa chỉ IP mà bạn muốn thiết lập cho Raspberry Pi (lưu ý để /24 ở cuối, hoặc tùy theo dải mạng của bạn, thông thường là /24) |
|--------------|--------------|
|**static routers** |Địa chỉ IP Gateway, ở gia đình thì thường nó là địa chỉ IP của modem/router luôn.|
|--------------|--------------|
|**static domain_name_servers** | Địa chỉ IP DNS phân giải tên miền. Thông thường chúng tôi dùng DNS của Google và OpenDNS. Bạn có thể thêm nhiều DNS, mỗi cái cách nhau bằng một dấu cách (khoảng trắng) |

```shell
# reboot
sudo reboot
# check ip 
ifconfig
```
