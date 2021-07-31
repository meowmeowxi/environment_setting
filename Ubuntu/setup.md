###Windows10安装Ubuntu双系统安装
本来以为是很容易的活，结果其中坎坷远远超出预期，特记录如下
1. 制作启动U盘
参考https://www.cnblogs.com/masbay/p/10745170.html ，发现台式机型号为UEFIbios+单硬盘，根据教程C往下走。进行磁盘分区、U盘制作，开始安装。其中关闭BIOS安全启动参考教程https://zhuanlan.zhihu.com/p/88531248 ,分配空间参考https://blog.csdn.net/Jesse_Mx/article/details/61425361  
问题：①分配空间有大问题。参考上述知乎连接，只分三个区，说硬盘too old（重启） ②参考原始教程，分四个区包括efi也说too old(重启) ③果然要关机安装！！关机后按照四个分区好了。但是文件的upgrade还有问题，出现了黑屏。按ESC进入安全模式。无效https://www.cnblogs.com/masbay/p/10718514.html 。无效https://zhuanlan.zhihu.com/p/50445643。  无效 https://blog.csdn.net/qq_37774098/article/details/118119513  
2. 最后，删除干净是安装的第一步:),参考 https://houkaifa.com/2019/08/15/ubuntu-uninstall/ 卸载分区和启动盘符，最后参考https://blog.csdn.net/guikunchen/article/details/88077330?utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-3.control&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-3.control ，卸载BOOT中的文档  
失败告终。算了，姐不伺候了，拜拜您嘞
