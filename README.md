# 一、文件说明
1. clover文件是 x1 carbon 2017 Catalina 10.15.4的EFI文件里的clover文件夹
   （clover is the EFI file for x1 carbon 2017 on Catalina 10.15.4）
2. OC是 x1 carbon 2017 在 Ventura 13.1 系统 引导为 OC 的EFI文件,此版本EFI文件将作为常更新的版本，推荐使用。
   （OC is the EFI file for x1 carbon 2017 on Ventura 13.1 with OC bootloader，and will be updated after changing）

# 二、硬件配置
x1 carbon 2017:
- CPU: i7-7600U
- GPU: HD620
- SSD: 970 EVO 1T

- SCREEN: 1080P
- WIFI: BCM94360CS2(已更换)
- SYSTEM: MACOS(单系统)

# 三、注意（tips）：
## 1. 使用建议（Some suggestions）

两个版本使用的时候建议更换三码后使用。并且我驱动里放了博通网卡的驱动，请自行去掉。（我OC的文件里三码删除掉了，请加入三码后才能正常使用）
（No matter which version, i advice you add the smbios and use it. And if you haven't replaced your wifi with bircm wifi, please remove the relevant kext in kext/other/(clover) or kext/(OC,and change the config.plist)）

## 2.黑果情况-这里只介绍OC引导的黑果状况（how is the hachintosh on my laptop just in OC going）

- thunderbolt热拔插存在问题
  雷电口扩展坞不支持热插拔（Hot plug is not supported on thunderbolt port）
- 睡眠后外接设备唤醒问题
  hackintosh equippment can not wake up from hibernation via external bluetooth or 2.4G device(such as mouse or keyboard). what make this happened is that a series of 060D renaming patched are used which can block the usb port when hibernating.

# 四、更新日志（changelog）:

| 序号 |    时间    |      OC版本      |      系统版本       |                           改动内容                           |
| :--: | :--------: | :--------------: | :-----------------: | :----------------------------------------------------------: |
|  1   | 2021.12.23 | OC version 0.7.6 |    Monterey 12.1    |                         更新 OC 版本                         |
|  2   | 2021.12.27 | OC version 0.7.6 |    Monterey 12.1    | 添加驱动 CpuTscSync.kext 来尝试修复睡眠唤醒后的的冻屏现象（有待验证结果） |
|  3   | 2022.01.03 | OC version 0.7.6 |    Monterey 12.1    | 之前的冻屏现象依然存在，不插电源会随机性的触控板和键盘没有反应，只有屏幕亮着，毫无反馈。本次更新内容为回退配置，并修补了核显的framebuffer相关参数 |
|  4   | 2022.01.13 | OC version 0.7.7 | Monterey 12.2 beta1 | 更新OC版本0.7.7，新增启动界面<br />冻屏现象已解决，把bcm94360cs2的转接卡重新插拔一下就好了 |
|  5   | 2022.01.25 | OC version 0.7.7 |    Monterey 12.1    | 又更新了，具体更新内容：本次EFI文件的改动内容为：<br />1.核显的properties改动，修复连接HDMI外接显示器开机导致的黑屏现象；<br />2.干掉了看门狗（watchdog）panic |
|  6   | 2022.02.18 | OC version 0.7.8 |    Monterey 12.2    | 更新了Cputscsync.kext debug 版本，果然卡死的现象消失了，看来的确是因为cpu 线程同步的原因 |
|  7   | 2022.03.08 | OC version 0.7.9 |   Monterey 12.2.1   |                 日常更新oc引导版本和各种驱动                 |
|  8   | 2022.04.19 | OC version 0.8.0 |  Monterey  12.3.1   | 1. 更新OC引导0.8.0<br>2.利用VoodooRMI.kext替代VoodooPS2-->Trackpad和mouse，提升使用体验<br>3.利用ecEnhancer.kext代替原有acpi和patch<br />4.其他一些小改动 |
|  9   | 2022.06.07 | OC version 0.8.1 |    Monterey 12.4    | 1. 更新OC引导0.8.1<br />2. 另外 MacOS 13 终于出咯，感觉还不错，本来打算这个笔记本Monterey 以后就不在往上升级了，但现在一看新增功能还不错，打算这个笔记本再追一个大版本>_< |
|  10  | 2020.07.13 | OC version 0.8.2 | Ventura 13.0 beta3  | 1.更新 Vetura 13.0 第一个公测版，目前使用稳定<br />2.更新OC 0.8.2 |
|  11  | 2022.08.03 | OC version 0.8.3 | Ventura 13.0 beta4  | 1.更新 Vetura 13.0 beta4版本，目前使用稳定<br />2.更新OC 0.8.3 |
|  12  | 2022.12.29 | OC version 0.8.7 |    Ventura 13.1     |   1.更新Ventura 13.1版本，目前使用稳定<br />2.更新OC 0.8.7   |
|  13  | 2023.01.03 | OC version 0.8.8 |    Ventura 13.1     |                1.更新OC 0.8.8以及一些常用驱动                |
|      |            |                  |                     |                                                              |
