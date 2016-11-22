# strongswan的下载、编译、安装
#### 下载 strongswan
wget https://download.strongswan.org/strongswan-5.5.1.tar.gz
#### 编译 strongswan
cd strongswan-5.5.1

./configure --prefix=/usr --sysconfdir=/etc

###### error1 缺少gmp库。
下载安装gmp库：
wget https://gmplib.org/download/gmp/gmp-6.1.1.tar.bz2
tar -xvf gmp-6.1.1.tar.bz2
cd gmp-6.1.1
./configure
make
make check
make install

###### 继续安装strongswan
./configure --prefix=/usr --sysconfdir=/etc
make
su
make install
