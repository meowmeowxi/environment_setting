基于Ubuntu容器内实现mongo+node通信(探索的过程)
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
![mongostart](../assets/Docker/mongostart.png)
#### 6. 安装node
`sudo apt-get install nodejs`,`sudo apt-get install npm`
#### 为映射文件夹，需要新建容器，但现有容器已下载了一些数据，故考虑先更新镜像，再基于更新后的镜像新建容器
#### 7. 更新镜像
`docker commit -m="has update" -a="miao" nju_ubuntu test_ubuntu:v2`  
https://www.runoob.com/docker/docker-image-usage.html
#### 8.映射文件夹
 `docker run -itd -v /home/miao/code/ubuntu-test/nju-mongo/:/data/db/ -v /home/miao/code/ubuntu-test/:/ubuntu-test/ --name=nju-ubuntu test_ubuntu:v2`  
 ![folder](../assets/Docker/folder.png)
