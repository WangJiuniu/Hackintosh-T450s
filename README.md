# Hackintosh安装成功指南（保姆级教程）
## 综述

本文以T450s安装MacOS系统的过程为例，讲述目前安装Hackintosh的常用方法和资源。安装过程是在win7系统中制作系统盘，然后根据设计的引导进行启动和系统安装。主要参考的教程包括“[黑果小兵的部落格](https://mp.weixin.qq.com/s/4_djpn_u3_nmPvCMGHR-dw)”微信公众号，以及[聪聪黑苹果安装工具3.0](https://www.bilibili.com/s/video/BV1iE41157Vd)。  本文讲述的方法是使用黑果小兵的教程制作系统盘，然后驱动聪聪黑苹果做好的系统进行安装，所以单一采用某一种方案时没有成功的读者可以考虑尝试本文介绍的方案。此外，本文也将详细阐述Intel N7265无线网卡如何安装WIFI等核心驱动。

## 系统盘制作

首先按照[黑果小兵](https://mp.weixin.qq.com/s/4_djpn_u3_nmPvCMGHR-dw)的教程下载dmg镜像（需要在公众号中打赏获得下载链接），然后用etcher软件将dmg镜像安装到u盘中。接着根据[列表](https://blog.daliansky.net/Hackintosh-long-term-maintenance-model-checklist.html)中的EFI进行尝试，采用DiskGenis软件将EFI文件进行替换。顺利的话，此时再稍微调整BIOS就能够安装成功，但不幸的是很多人都会卡在某一条命令上。

此时就可以尝试第二种安装方法，由[聪聪黑苹果](https://www.bilibili.com/s/video/BV1iE41157Vd)提供的安装工具也很专业。按照工具的视频教程，下载img格式的镜像，然后将镜像和之前找到的[EFI](https://blog.daliansky.net/Hackintosh-long-term-maintenance-model-checklist.html)拖动到软件中，选择合适的硬盘，将MacOS系统直接安装到硬盘中。然后调整BIOS，以硬盘启动进入MacOS官方安装界面。可是事情偏偏又不顺利，在T450s机器上，安装工具不能正确地生成CCMac引导，导致无法进入从BIOS硬盘。

两次失利之后，偶然间将两种方法结合起来获得成功。采用黑果小兵的在U盘中做出的OC引导，进入聪聪黑苹果的CCMac引导，完成安装。

这一过程的详细步骤和教程请点击[这里](https://github.com/WangJiuniu/Hackintosh-T450s/tree/main/make_system_oc)。


## 系统安装

正常进入系统后，安装过程按照聪聪黑苹果提供的[视频](https://www.bilibili.com/s/video/BV1iE41157Vd)进行即可。

## EFI设置及WIFI驱动、声卡驱动安装

安装完之后，由于EFI是在U盘中，需要按照黑果小兵的教程将EFI从U盘拷贝到系统硬盘。

此外，由于无线网卡型号与原EFI不符合，只能使用网线联网。因此需要进行Intel无线网卡的驱动安装。

这一过程的详细步骤和教程请点击[这里](https://github.com/WangJiuniu/Hackintosh-T450s/tree/main/EFI_and_WIFI)。

## Mac系统使用中的优化

系统安装完成后，仍然有一些细节可以提升整体体验（如：键盘键位设置）。这一过程的详细步骤和教程请点击[这里](https://github.com/WangJiuniu/Hackintosh-T450s/tree/main/system_trick)。

## 总结

尽管有很多的教程和工具，Hackintosh的安装仍然主要面向发烧友。一些教程说的很简单，但是遇到安装问题时，新手很难解决。这篇文章旨在阐述安装过程、列举相关资源，同时对过程中的一些概念进行普及。



