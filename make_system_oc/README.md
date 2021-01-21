## 系统盘制作

此处介绍的方案综合使用[黑果小兵](https://mp.weixin.qq.com/s/4_djpn_u3_nmPvCMGHR-dw)和[聪聪黑苹果](https://www.bilibili.com/s/video/BV1iE41157Vd)。

(1) 在[黑果小兵](https://mp.weixin.qq.com/s/4_djpn_u3_nmPvCMGHR-dw)公众号中打赏获得dmg镜像链接。

(2) 用etcher软件将dmg镜像安装到u盘中。dmg镜像里面包含了MacOS系统，需要16GB或更高容量的U盘。

(3) 由于不同设备所需要的驱动不同，需要寻找适合目标机器的驱动来安装MacOS，系统盘中的引导称作EFI。EFI是决定系统能否安装成功和安装过后兼容程度的关键。好在大神们已经整理好[列表](https://blog.daliansky.net/Hackintosh-long-term-maintenance-model-checklist.html)，直接将列表中机型对应项目都下载下来，逐个尝试EFI即可。

(3) 采用DiskGenis软件将U盘中的EFI文件进行替换，这一步的教程请点击[这里](https://blog.csdn.net/weixin_39568597/article/details/112588714)。

(4) 顺利的话，此时再稍微调整BIOS的启动硬盘顺序、引导方式等就能进行安装，但不幸的是很多人都会卡在某一条命令上。顺便科普一下，BIOS支持采用的引导方式包括UEFI和Legacy，本文中MacOS的引导采用UEFI方式。T450s机型中，采用重置默认BIOS设置即可。引导安装系统时卡代码现象大多是EFI的设置问题，不需要在BIOS设置中花费太多时间。

(5) 由于同一机型往往也有不同硬件，[列表](https://blog.daliansky.net/Hackintosh-long-term-maintenance-model-checklist.html)中的EFI并不是万能的。大神往往会参照[文档](https://mp.weixin.qq.com/s/rvWIiXAhlo10IAs2MIm4Gg)修改EFI，但是一般读者可以采用本文介绍的方法进行。

(6) 尝试第二种安装方法，采用由[聪聪黑苹果](https://www.bilibili.com/s/video/BV1iE41157Vd)提供的安装工具。聪聪黑苹果工具[官网](http://ccmacos.cn/)，点击[资源](http://ccmacos.cn/#contact)进入下载页。

(7) 聪聪黑苹果工具使用参考视频即可，需要注意的是工具中使用的镜像要求是img格式的，根据[资源](http://ccmacos.cn/#contact)中的提示下载压缩包，解压后的txt文件中记录了下载地址。

(8) 将img镜像和适合本机的EFI拖入聪聪黑苹果工具，对目标硬盘进行系统安装。然后按要求进行引导修复，生成CCMacOS的引导项。 

(9) 按照[视频](https://www.bilibili.com/s/video/BV1iE41157Vd)中的说法，如果引导修复成功后，可以直接进入硬盘进行安装，但是T450s没有引导修复报错。故转而采用根据黑果小兵制作的U盘进行引导，进入引导系统后点击CCMacOS启动项。


[返回首页](https://github.com/WangJiuniu/Hackintosh-T450s)