### Windows10安装Ubuntu双系统安装
本来以为是很容易的活，结果其中坎坷远远超出预期，特记录如下
1. 制作启动U盘
参考https://www.cnblogs.com/masbay/p/10745170.html ，发现台式机型号为UEFIbios+单硬盘，根据教程C往下走。  
进行磁盘分区、U盘制作，开始安装。其中关闭BIOS安全启动参考教程https://zhuanlan.zhihu.com/p/88531248 ,分配空间参考https://blog.csdn.net/Jesse_Mx/article/details/61425361   
问题：①分配空间有大问题。参考上述知乎连接，只分三个区，说硬盘too old（重启） ②参考原始教程，分四个区(efi)也说too old(重启) ③ 原来是要windows关机后再安装，不能是重启状态，关机后按照四个分区安装好了  
④进入系统后经常出现文件读写错误，反复多次后发现是要Windows重启状态下进入Ubuntu才可以。但是我最后一次实验的时候，先upgrade测试了一下，果真出现了文件读写问题，可惜这时候就无法正常关机了，强制关机后再次进入呈现黑屏状态。网上很多人说是NVIDIA文件的问题，参考以下三个教程进行了三次测试还是无法进入，综合考虑多种因素后舍弃了双系统。按ESC进入安全模式。无效https://www.cnblogs.com/masbay/p/10718514.html 。无效https://zhuanlan.zhihu.com/p/50445643。  无效 https://blog.csdn.net/qq_37774098/article/details/118119513  
2. 最后，删除干净是安装的第一步:),参考 https://houkaifa.com/2019/08/15/ubuntu-uninstall/ 卸载分区和启动盘符，打不开的话可以参考https://blog.csdn.net/qq_41196190/article/details/105353318 ，最后参考https://blog.csdn.net/guikunchen/article/details/88077330?utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-3.control&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-3.control ，卸载BOOT中的文档  
失败告终。算了，姐不伺候了，拜拜您嘞
