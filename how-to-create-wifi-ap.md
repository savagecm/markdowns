#将代码copy到本地，安装
git clone https://github.com/oblique/create_ap
cd create_ap
make install

#安装依赖的库
apt-get install util-Linux procps hostapd iproute2 iw haveged dnsmasq

#创建WiFi热点（GitHub上有多种方式创建，可以查找自己需要的那种）
sudo create_ap wlan0 eth0 热点名 密码

#开机启动
将sudo create_ap wlan0 eth0 热点名 密码 添加到/etc/rc.local当中，即可开机启动
