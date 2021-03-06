### 1. anaconda新建虚拟环境PyTorch
![anaconda虚拟环境配置](../assets/anaconda-create.png)  
### 2. 激活虚拟环境
命令行输入`conda activate PyTorch`  
![激活虚拟环境](../assets/active-environment.png)   
注：若未设置环境变量，可参考 https://blog.csdn.net/mars_xiaolei/article/details/82798640
### 3. 安装PyTorch
①查看cuda版本
桌面右键→NVIDA控制面板→系统信息→组件→产品名称
![cuda版本](../assets/nvida-version.png)  
②复制conda命令
进入PyTorch官网https://pytorch.org/get-started/locally/ ,选择目标系统配置，复制conda命令  
![复制conda命令](../assets/pytorch-download.png)  
③命令行安装PyTorch  
![安装PyTorch](../assets/pytorch-setup.png) 
注：若显示包不可用，可从清华镜像重新下载 https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/win-64/
### 4. 测试是否安装成功
```
import torch
torch.cuda
torch.cuda.is_available()
```
若结果为True，则证明安装成功
![测试torch](../assets/torch-test.png) 
### 5.在特定文件夹打开jupyter notebook
命令行输入`jupyter notebook` 
