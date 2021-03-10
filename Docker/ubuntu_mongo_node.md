基于Ubuntu容器内实现mongo+node通信
#### 1. 拉取ubuntu镜像
`docker pull ubuntu`  
#### 2. 启动ubuntu容器
`docker run -itd --name miao-ubuntu ubuntu`
#### 3. 进入容器
`docker exec -it miao-ubuntu bash`
#### 4. 安装sudo
`apt-get update`,`apt-get install sudo`
#### 5. 安装mongodb
`sudo apt install mongodb`  
报错①输入`mongo`测试，connection attempt failed mongo.js:257:13  
解决方案：https://stackoverflow.com/questions/51812931/does-not-start-mongodb-4  
#### 5. 安装node
`sudo apt-get install nodejs`,`sudo apt-get install npm`
