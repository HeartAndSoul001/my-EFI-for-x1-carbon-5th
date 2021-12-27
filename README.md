# 一、文件说明
clover文件是 x1 carbon 2017 Catalina 10.15.4的EFI文件里的clover文件夹
（clover is the EFI file for x1 carbon 2017 on Catalina 10.15.4）
myOCEFI是 x1 carbon 2017 在 monterey 12.1 系统 引导为OC 0.7.6 的EFI文件,此版本EFI文件将作为常更新的版本
（myOCEFI is the EFI file for x1 carbon 2017 on big sur 12.1 with OC bootloader 0.7.6，and will be updated after changing）

# 二、硬件配置
x1 carbon 2017:
CPU: i7-7600U
GPU: HD620
SSD: 970 EVO 1T
SCREEN: 1080P
WIFI: BCM94360CS2(已更换)
SYSTEM: MACOS(单系统)

# 三、注意（tips）：
## 1.使用建议（Some suggestions）

两个版本使用的时候建议更换三码后使用。并且我驱动里放了博通网卡的驱动，请自行去掉。（我OC的文件里三码删除掉了，请加入三码后才能正常使用）
（No matter which version, i advice you add the smbios and use it. And if you haven't replaced your wifi with bircm wifi, please remove the relevant kext in kext/other/(clover) or kext/(OC,and change the config.plist)）

## 2.黑果情况-这里只介绍OC引导的黑果状况（how is the hachintosh on my laptop just in OC going）

- thunderbolt热拔插存在问题
  雷电口扩展坞不支持热插拔（Hot plug is not supported on thunderbolt port）
- 睡眠后外接设备唤醒问题
  hackintosh equippment can not wake up from hibernation via external bluetooth or 2.4G device(such as mouse or keyboard). what make this happened is that a series of 060D renaming patched are used which can block the usb port when hibernating.

# 四、更新日志（changelog）:

| 序号 |    时间    |      OC版本      |   系统版本    |                           改动内容                           |
| :--: | :--------: | :--------------: | :-----------: | :----------------------------------------------------------: |
|  1   | 2021.12.23 | OC version 0.7.6 | Monterey 12.1 |                         更新 OC 版本                         |
|  2   | 2021.12.27 | OC version 0.7.6 | Monterey 12.1 | 添加驱动 CpuTscSync.kext 来尝试修复睡眠唤醒后的的冻屏现象（有待验证结果） |
|      |            |                  |               |                                                              |

