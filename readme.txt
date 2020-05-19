# chromebook-install-linux-app

1、启用Linux（Beta）
2、sudo apt-get -y update && apt-get -y upgrade && apt-get -y dist-upgrade
3、增加中文支持 dpkg-reconfigure locales
4、从win7移植字体：将字体复制到wps_symbol_fonts文件夹，
sudo mv wps_symbol_fonts /usr/share/fonts/
cd /usr/share/fonts/wps_symbol_fonts/
sudo mkfontscale
sudo mkfontdir
sudo fc-cache
5、安装wps：运行deb文件
6、安装输入法
7、安装wqy字体文件
