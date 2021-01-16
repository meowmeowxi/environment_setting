实现docker容器间的通信
#### 1. 新建内部网络
新建： `docker network create miao-test`  
展示： `docker network ls`  
![docker network](../assets/Docker/network.png)
#### 2. 新建项目文件夹
新建文件夹nju： `mkdir nju`  
新建文件夹nju的子文件夹nju-mongo：`mkdir nju-mongo` 
#### 3. 初始化node项目
在nju文件夹里初始化node：`npm init`  
新建index.js `vim index.js`  
安装包`npm install express --registry=https://registry.npm.taobao.org`、`npm install mongodb --registry=https://registry.npm.taobao.org`  
![npm install](../assets/Docker/npm-install.png)
#### 4.开启mongo容器
开启：`docker run -d -v /home/miao/code/nju/nju-mongo/:/data/db/ --name nju-mongo --network miao-test --network-alias nju-mongo mongo`  
查看: `docker ps`  
![npm install](../assets/Docker/mongo-network.png)
