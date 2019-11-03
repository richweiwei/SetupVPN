# 1.快速在新服务器上搭建VPN服务

# #为方便下载，在settings中把res设置为公开

1、在新服务器上下载并安装vpnsetup

 wget https://raw.githubusercontent.com/richweiwei/SetupVPN/master/vpnsetup.sh -O vpnsetup.sh && sh vpnsetup.sh

2、修改github上vpn.mobileconfig文件的IP地址,修改为新服务器ip,提交github

https://github.com/richweiwei/SetupVPN/blob/master/vpn.mobileconfig

3、在新服务器上安装nginx【可选】

sudo apt update && sudo apt install nginx

4、在nginx目录下/var/www/html目录下载github上的vpn.mobileconfig文件【可选】

cd /var/www/html && wget https://github.com/richweiwei/SetupVPN/raw/master/vpn.mobileconfig -O vpn.mobileconfig

5、把http/newip/vpn.mobileconfig发送到iOS，由safari浏览打开，按提示安装vpn配置文件

5.1 优先尝试【成功的话不需要步骤3/4】

https://github.com/richweiwei/SetupVPN/raw/master/vpn.mobileconfig

5.2 github下载不了， 从新服务器下载

http/1.2.3.4/vpn.mobileconfig

# #为了安全，在settings中把res设置为私有


# 2.管理vpn用户，请下载该github下的脚本

https://github.com/hwdsl2/setup-ipsec-vpn/blob/master/docs/manage-users.md
