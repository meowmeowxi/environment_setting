### 容器的形式
#### 导出容器
#### 1. 进入希望放置导出包的目录
#### 2. 查看导出容器的id
`docker ps -a`
#### 3. 导出容器
`docker export 7658a88ea270 >node.tar`，7658a88ea270是container id，node.tar是名字  
![导出镜像](../assets/Docker/export.png) 

#### 导入容器
#### 1. 进入放置导入包的目录
#### 2. 导入容器
`docker import - my-mongo <mongo.tar`
### 镜像的形式
#### 1.导出镜像
`docker save nju-ubuntu4 > test_ubuntu.tar`
#### 2.导入镜像
`docker load < test_ubuntu.tar`  
https://www.hangge.com/blog/cache/detail_2411.html
