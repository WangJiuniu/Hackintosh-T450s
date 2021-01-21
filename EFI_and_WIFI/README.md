## EFI设置及WIFI驱动、声卡驱动安装

### EFI设置

由于是采用U盘进行引导，仍然需要根据黑果小兵的[教程](https://mp.weixin.qq.com/s/4_djpn_u3_nmPvCMGHR-dw)，将U盘中的EFI拷贝到硬盘中。教程PDF已经分享在"【黑果小兵】Big Sur安装教程.pdf"中。实际执行
"安装后的系统设置"(不确定是否必要，因为报错了但不影响使用)和"将U盘中的EFI复制进硬盘 - 工具篇"。自此已经完成了系统主体的安装，支持拔出U盘重启系统。

### WIFI驱动安装

此外，由于无线网卡型号与原EFI不符合，只能使用网线联网。
因此需要进行Intel无线网卡的驱动安装，可以参考[视频教程](https://www.youtube.com/watch?v=i8XRv6VrV6g&ab_channel=KUMI%E5%88%86%E4%BA%AB)进行，采用[HeliPort](https://github.com/OpenIntelWireless/HeliPort)结合[itlwm](https://github.com/OpenIntelWireless/itlwm)方案。驱动文件为"itlwm.kext"，安装方式可以使用OpenCore软件，驱动安装方式教程可以参考另一个[视频教程](https://www.youtube.com/watch?v=kJAz92cqavA&t=256s&ab_channel=KUMI%E5%88%86%E4%BA%AB)(注：本文引用此教程旨在说明OpenCore的使用)。

当然采用安卓手机USB共享网络也挺好的，方便且稳定，双击安装"HoRNDIS-x.pkg"即可，[项目地址](https://github.com/jwise/HoRNDIS/releases)。

### 声卡驱动安装

仿冒声卡的难度太大，使用万能声卡"VoodooHDA.OC.dmg"也挺好的，[视频教程及下载地址](https://www.youtube.com/watch?v=GBDCQBqf4_k&ab_channel=chris1111)。

[返回首页](https://github.com/WangJiuniu/Hackintosh-T450s)