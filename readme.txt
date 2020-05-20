# chromebook-install-linux-app

1、启用Linux（Beta）
2、sudo apt-get -y update && apt-get -y upgrade && apt-get -y dist-upgrade
3、增加中文支持 dpkg-reconfigure locales
4、从win7移植字体：
将字体复制到wps_symbol_fonts文件夹
修改字体文件权限 chmod 666 ./*
sudo mv wps_symbol_fonts /usr/share/fonts/
cd /usr/share/fonts/wps_symbol_fonts/
sudo mkfontscale
sudo mkfontdir
sudo fc-cache
5、安装wps：运行deb文件
6、安装输入法
sudo apt install fcitx
im-config，点击确定->点击Yes->选择fcitx->确定->确定，重启使配置生效
sudo apt-get install fcitx-libpinyin
重启
运行fcitx
运行fcitx-config-gtk3，添加输入法
sudo vi /etc/systemd/user/cros-garcon.service.d/cros-garcon-override.conf
在文件末尾添加三行
Environment="GTK_IM_MODULE=fcitx"
Environment="QT_IM_MODULE=fcitx"
Environment="XMODIFIERS=@im=fcitx"
保存
sudo vi ~/.sommelierrc
在这个新文件中添加一行
/usr/bin/fcitx-autostart
保存
重启
7、安装wqy字体文件
sudo apt install fonts-wqy-microhei fonts-wqy-zenhei
