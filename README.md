# 一、文件说明
clover文件是 x1 carbon 2017 Catalina 10.15.4的EFI文件里的clover文件夹
（clover is the EFI file for x1 carbon 2017 on Catalina 10.15.4）
myOCEFI是 x1 carbon 2017 在 monterey 12.1 系统 引导为 OC 的EFI文件,此版本EFI文件将作为常更新的版本
（myOCEFI is the EFI file for x1 carbon 2017 on big sur 12.1 with OC bootloader，and will be updated after changing）

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

| 序号 |    时间    |      OC版本      |      系统版本       |                           改动内容                           |
| :--: | :--------: | :--------------: | :-----------------: | :----------------------------------------------------------: |
|  1   | 2021.12.23 | OC version 0.7.6 |    Monterey 12.1    |                         更新 OC 版本                         |
|  2   | 2021.12.27 | OC version 0.7.6 |    Monterey 12.1    | 添加驱动 CpuTscSync.kext 来尝试修复睡眠唤醒后的的冻屏现象（有待验证结果） |
|  3   | 2022.01.03 | OC version 0.7.6 |    Monterey 12.1    | 之前的冻屏现象依然存在，不插电源会随机性的触控板和键盘没有反应，只有屏幕亮着，毫无反馈。本次更新内容为回退配置，并修补了核显的framebuffer相关参数 |
|  4   | 2022.01.13 | OC version 0.7.7 | Monterey 12.2 beta1 |                更新OC版本0.7.7，新增启动界面                 |
|  5   | 2022.01.25 | OC version 0.7.7 |    Monterey 12.1    | 又更新了，具体更新内容：这段时间我回到了windows环境下，更新了最新的Thinkpad的bios版本，此举动为了修复序号3中的冻屏现象，怀疑是intel对cpu底层做了改动，导致苹果也对intel版本的mac底层的东西做了修改；查看Thinkpad x1 carbon 2017最新的bios驱动，更新内容也确实涉及到cpu微码的更新，具体如下：<br /><1.53>：<br />UEFI: 1.53 / ECP: 1.22<br />\- [重要] 更新包括安全修复.<br />\- (新增) 更新CPU微码.<br />\- (修正) 安装 OPAL 管理软件时通过 Windows Update 更新设备固件失败的问题.<br /><br />本次EFI文件的改动内容为：<br />1.核显的properties改动，修复连接HDMI外接显示器开机导致的黑屏现象；<br />2.干掉了看门狗（watchdog）panic |

