Trước khi đi vào cài đặt các bác cần vào đây để nhận License 15 ngày của Cpanel nhé: Link nhận License

https://cpanel.net/products/trial/

cài đặt thư viện

```
yum install perl
yum install curl
```

Tắt Selinux

```
sed -i ‘s/SELINUX=/#SELINUX=/g’ /etc/selinux/config
SELINUX=disabled >> /etc/selinux/config
```
Lưu ý: nếu k dùng được lệnh thì vào nano /etc/selinux/config
đổi thành `SELINUX=disabled` là được


Tắt Network Manager
```
systemctl stop NetworkManager.service
systemctl disable NetworkManager.service
```

Khởi động lại Network

```
systemctl enable network.service
systemctl start network.service
```

Update VPS

```
yum update -y
```

Install Cpanel

```
cd /home
curl -o latest -L https://securedownloads.cpanel.net/latest
sh latest
```



link tham khảo: https://datnguyentv.com/install-cpanel-free-license-15-days/
