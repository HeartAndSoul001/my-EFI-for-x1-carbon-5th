# my-EFI-for-x1-carbon-5th
clover文件是 x1 carbon 2017 Catalina 10.15.4的EFI文件里的clover文件夹
（clover is the EFI file for x1 carbon 2017 on Catalina 10.15.4）
myOCEFI是 x1 carbon 2017 Catalina 10.15.4 的EFI文件
（myOCEFI is the EFI file for x1 carbon 2017 on Catalina 10.15.4）

x1 carbon 2017:
CPU: i7-7600U
GPU: HD620
SSD: 970 EVO 1T
SCREEN: 1080P
WIFI: BCM94360CS2(已更换)
SYSTEM: MACOS(单系统)

注意（tips）：
1. 两个版本使用的时候建议更换三码后使用。并且我驱动里放了博通网卡的驱动，请自行去掉。（我OC的文件里三码删除掉了，请加入三码后才能正常使用）
（No matter which version, i advice you add the smbios and use it. And if you haven't replaced your wifi with bircm wifi, please remove the relevant kext in kext/other/(clover) or kext/(OC,and change the config.plist)）

黑果情况（这里只介绍OC引导的黑果状况）：how is the hachintosh on my laptop just in OC:
除了thunderbolt热拔插、hdmi有小问题其他一切正常
（everything is ok except thunderbolt,hdmi）
