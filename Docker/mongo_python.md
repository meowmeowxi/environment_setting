基于mongodb和python配置网站后端环境，其中mongod、python、adminmongo(mongodb可视化管理工具)放再docker内，code server 放在映射文件夹内
#### 1. 拉取Mongo镜像
`docker pull mongo`  
#### 2. 启动docker容器
`docker run -itd -v /code/docker/backend/:/data/db/ --name= backend mongo`
#### 3. 容器内安装python
```
apt-get update
apt-get upgrade
apt install build-essential -y
apt install libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev -y
apt install zlib1g-dev
apt install wget
apt install openssl
apt install curl
apt install libsqlite3-dev
```
考虑到wget下载较慢，采取windows直接下载，然后导入docker的形式
①windows下载`https://www.python.org/ftp/python/3.7.3/Python-3.7.3.tgz`
②`docker cp Python-3.7.3.tgz backend:/nju`
```
tar -xvf Python-3.7.3.tgz
cd Python-3.7.3
./configure —enable-loadable-sqlite-extensions
make
make install
apt-get clean
ln -s /usr/local/bin/pip3 /usr/bin/pip
ln -s /usr/local/bin/python3 /usr/bin/python
```
参考：https://blog.csdn.net/GeneralJing/article/details/114474999  
注：直接使用apt install python，输入python无法进入命令行，可能是环境变量的问题
