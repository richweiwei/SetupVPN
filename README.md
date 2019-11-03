# SetupVPN

1、在新服务器上下载并安装vpnsetup

 wget https://raw.githubusercontent.com/richweiwei/SetupVPN/master/vpnsetup.sh -O vpnsetup.sh && sh vpnsetup.sh

2、修改github上vpn.mobileconfig文件的IP地址,修改为新服务器ip,提交github

https://github.com/richweiwei/SetupVPN/blob/master/vpn.mobileconfig

3、在新服务器上安装nginx

sudo apt update && sudo apt install nginx

4、在nginx目录下/var/www/html目录下载github上的vpn.mobileconfig文件

wget https://github.com/richweiwei/SetupVPN/raw/master/vpn.mobileconfig -O vpn.mobileconfig

5、把http/newip/vpn.mobileconfig发送到iOS，由safari浏览打开，按提示安装vpn配置文件

http/1.2.3.4/vpn.mobileconfig
