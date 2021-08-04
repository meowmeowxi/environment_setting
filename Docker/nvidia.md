### Docker + WSL2 配置NVIDIA
1. 升级OS Builder.
下载PC Health Check https://docs.microsoft.com/zh-cn/windows/win32/direct3d12/gpu-cuda-in-wsl ，检查电脑是否符合要求。参考https://baijiahao.baidu.com/s?id=1703970038037422511 、
https://zhuanlan.zhihu.com/p/383977287 开启TMP。加入微软体验计划，选择dev模式进行更新https://docs.microsoft.com/zh-cn/windows/win32/direct3d12/gpu-cuda-in-wsl
2. 安装CUDA
https://docs.nvidia.com/cuda/wsl-user-guide/index.html#installing-nvidia-drivers , CUDA tooltik版本选择了11.1 https://developer.nvidia.com/cuda-11.1.0-download-archive?target_os=Linux&target_arch=x86_64&target_distro=WSLUbuntu&target_version=20&target_type=debnetwork 。

卸载CUDA：由于重复安装了很多次，以为/usr/local下的cuda文件夹没用便删除了，结果是需要的，但重新安装的时候却提示已经安装好了cuda，因此需要先卸载cuda tooltik。  
 ```
 sudo apt-get remove cuda 
 sudo apt-get remove cuda*
 sudo dpkg -l |grep cuda #查看是否还含有相关文件
 sudo dpkg -P FILE-NAME-LIST # for example, sudo dpkg -P cuda-visual-tools-11-4 
 ```
