## 目录

* [本教程免责声明](#免责声明)
* [主要贡献者名单](#主要贡献者名单)

  * [紫光展锐处理器部分机型深刷破解(直接替换无限制版系统分区法)](#1紫光展锐处理器部分机型深刷破解)

    * [1.0该方案适用机型情况](#10该方案适用机型情况)
    * [1.1下载您需要的文件](#11下载您需要的文件)
    * [1.1.1 spd深刷驱动以及spd深刷工具的下载](#111spd深刷驱动以及spd深刷工具的下载)
    * [1.2 spd深刷的备份和刷写操作](#12-spd深刷的备份和刷写)
    * [附件 c6官刷版系统注意事项](#c6系统注意事项)
  * [高级教程：学习机系统制作官改版系统教程(仅a9)](#2学习机系统制作官改版系统教程)

    * [阅读要求](#20-阅读要求)
    * [文件准备](#21-文件准备)
    * [(修改system)修改system和vendor达成root](#22-修改system+vendor以root)
    * [(修改system)替换安装器](#23-修改system替换安装器)
    * [(修改boot)boot方法root](#24-bootboot方法root仅apatch)

# 免责声明

在开始破解设备及刷机之前，您需要知悉以下几点

1. 刷机有一定风险，有一定使设备完全损坏的可能，如果您无法保证您可以在操作之前确认您的技术不足以支持您破解此设备，或您无法保证您的设备不会因此损坏，请去淘宝或者讯飞线下店、官方维修去刷，价格保持在60~100元左右，若您执意自行操作，并因为误操作导致您的设备损坏，此文章编写团队概不负责。
2. 如果您需要的只是安装应用功能，并要求保留学习功能，请看我们的的官方侧载应用教程。
3. 此文章受众：因为各种情况，以后用不上学习机学习功能并希望将此机器废物利用的用户。
4. 未成年人请在家长允许并陪同+配合下进行刷机。如果您不同意\未获得家长允许并陪同\自认为自己技术不足的，请退出本文档，本文档部分章节已经超出了《科大讯飞AI学习机AI学习软件服务用户协议》： 用户若对学习机进行刷机行为，包括但不限于获取root权限，刷入第三方ROM等，则本机将会从科大 讯飞AI学习机官方技术支持和软件保修服务中被移除
5. 如果您未同意此条款或者未遵守本文第四条规定并因此带来的各种经济损失，精神损失，此文章编写团队概不负责。
6. 若您不同意以上条款，请您退出并在您的个人设备上删除此文档并不再操作

   # 主要贡献者名单

   @KawaiiSparkle/@qwqlemon2333/@whhh233一起编写了伪造apk更新包教程+Root教程

   @Tomking062提供了实操Root的思路(system-mode方法)、spd_dump工具(改进版本)

   @whhh233为我们免费提供了网盘来存放文件 目前因为腾讯云风控说他这个网盘可能有欺诈行为，所以他把 网盘关了

   @WalleoAndrew最初开始搞科大AI学习机解除安装限制的人,BOOM群群主

   @YedLeo1/@KawaiiSparkle研究出了 T20Pro 没有BL锁或启用的avb2.0验证 的结论。并在此基础上成功 Root了该机型，还初步适配了该机型的TWRP

   @KawaiiSparkle/@LYao2514创作了一键自动patch系统分区的脚本

   @永夜—x2向我证明了x2刷入x2pSystem的可能性

   酷安/Bilibili@某贼 帮助我们将一些镜像、文件转存到萤火虫资源站

   致谢部分到此结束

   ---

# 1.紫光展锐处理器部分机型深刷破解

此破解方法基于将学习机的system分区备份并替换为破解完成或官方解锁之后的system分区以达到删除学习功能并自由安装软件的目的，理论上紫光机型应该能通刷，只不过因为缺少刷机包资源支持，所以基本上只能破解的部分机型如下（若有偏差请指正）

## 1.0该方案适用机型情况

* X2/Z1/Q1/X3Pro/C6全系
* T10/T20/C8全系
* A10(仅理论)

  不能破解的机型

  任何高通、瑞芯微机型（若您有需要请移步高通、瑞芯微机型破解教程）

  Ud710-chip2/ad机型（缺少fdl文件）

  T310（ums312）机型（缺少fdl文件）

  ## 1.1下载您需要的文件

  您需要有一台电脑，并下载几个工具和适合您设备的刷机包

  ### 1.1.1spd深刷驱动以及spd深刷工具的下载

请您去这个网站下载 [网站](qutick102.ysepan.com)!

**并且下载图片内划线的文件**

![](https://www.helloimg.com/i/2025/03/06/67c97f4a53f70.png)

您还需要下载大部分展锐机型的fdl文件

请去群内或者我们的webdav下载

若您确定您有IPv6，那么请您http协议端口6066并匿名登陆即可

![ipv6地址](https://www.helloimg.com/i/2025/03/05/67c78d3444c26.png)

**若您无法确定您有没有ipv6请访问**

![ipv4地址](https://www.helloimg.com/i/2025/03/07/67cafb77cd525.jpg)

![文件位置](https://www.helloimg.com/i/2025/03/05/67c78d37c5f60.png)

![文件地址2](https://www.helloimg.com/i/2025/03/05/67c78d37be949.png)

2．刷机包下载地址 [萤火虫资源站](www.yhcres.top)

![萤火虫资源站](https://www.helloimg.com/i/2025/03/05/67c806c434359.png)

打开网站后，点击“03-学习机、家教机、学生卡、学生平板、儿童手机”按钮，此时会跳转到下一个页面，拉到最底下选择“讯飞”按钮即可**选择您需要刷写的==设备==**

![请您下载划线的文件](https://www.helloimg.com/i/2025/03/05/67c806c1d1f38.png)

例如科大讯飞x2pro，虽然没有，但是他的课堂版（学校特供吃回扣版）也就是C6的官解刷机包是可以通用的(==同样适用于x2==)，如果在未来找不到刷机包可以尝试刷写同芯片机型的刷机包，但是刷机之前一定要备份，下文会讲到，否则等着去找售后修吧！

下到刷机包之后，您应该打开这个文件 ，这个文件一般为.zip格式，请用解压软件将带有system字样的bin文件或img文件解压到一个存储足够大，且足够稳定的存储位置，并记着这个文件存储在哪

![move system.bin to flash](https://www.helloimg.com/i/2025/03/05/67c806c20bb0b.png)

现在您应该打开您刚刚下载的spd_dump_stable.zip和紫光驱动_R4.21.3201.zip

您应该先打开紫光驱动_R4.21.3201.zip并安装驱动

**==请您检查您的计算机的windows系统版本==**，并选择与您对应的驱动（例如windows7就应该选择DriversForWin78）

将与您计算机系统版本对应的文件夹解压到任意文件夹并且打开

![spd driver setup](https://www.helloimg.com/i/2025/03/05/67c806c2eeada.png)

请选择与您计算机cpu位数（x86/x32,x64）所对应的版本，大部分计算机应该选择DPInst64.exe

![spd dump 2](https://www.helloimg.com/i/2025/03/05/67c80cae1a6c7.png)

双击打开DPInst64.exe/ DPInst32.exe（以上文提到的您的计算机的字长为准），一般会弹出安装界面

您只需要一直点击下一步即可

![driver setup 1](https://www.helloimg.com/i/2025/03/05/67c80cad91c5e.png)

![Spd driver 2](https://www.helloimg.com/i/2025/03/05/67c80cadec656.png)

现在您需要解压另外一个文件“spd_dump_stable.zip”

![SPD 1](https://www.helloimg.com/i/2025/03/05/67c80cae0769f.png)

解压完成后点击SPRD文件夹，将您刚刚下载的两个fdl文件挪到这里，并确定这两个文件的名称是fdl1.bin和fdl2.bin

![Fdl move](https://www.helloimg.com/i/2025/03/05/67c80cae61053.png)

## 1.2 spd深刷的备份和刷写

1.按住音量减连接电脑

设备关机，打开深刷工具spd_dump.exe，在关机之后摁住设备音量减，并将设备插入计算机，如能看到如下图BROM＞字样，可松开按钮，如没有，请重启你的计算机和平板或者尝试在插入计算机前，将设备所有按键按住或按住音量加、功能键等。

![into spd on pc](https://www.helloimg.com/i/2025/03/06/67c980dbe224a.png)

2.进入fdl模式命令

在此之前先保证您的设备是Windows10或者Windows7，win11经过@Y2K-x2p的验证usb3成功链接概率很小

输入

`fdl fdl1.bin 0x5500`

回车，再输入

`fdl fdl2.bin 0x9efffe00`

您应该会进入这个界面

![in fdl 1](https://www.helloimg.com/i/2025/03/06/67c9832200b5c.png)

回车接着输入

`exec`

进入fdl2模式。

请您按照我写出的步骤执行，否则会失败（报错usb send fail），失败后请长摁平板关机键重启平板

若您看到下图界面，则说明您成功进入了fdl模式

![in fdl 2](https://www.helloimg.com/i/2025/03/07/67ca29ff380c0.png)

## 1.3备份全盘

您先需要备份全盘分区并妥善保存，输入

`r all`

意为读取全盘

即可，如果软件闪退，可以从头再来，在r all时加入目标地址 ，但是不管怎样，文件都会保存SPRD文件夹内（您打开工具的文件夹）

![R system](https://www.helloimg.com/i/2025/03/07/67ca2b72e19a3.png)

等文件读取完毕，你应该去把文件妥善保存并记住存储位置

![R system 2](https://www.helloimg.com/i/2025/03/07/67ca2c5f43d00.png)

应该输出类似于此，此为全盘备份图片

## 1.4刷入之前破解好的system.bin

解压之前在萤火虫或者文件站下载的刷机包，记住解压后system.bin文件的路径位置，如：I:\x2pro-system.bin。

在刷机工具spd_dump.exe窗口内输入

`w system I:\x2pro-system.bin`

（注意文件名不能有空格）

等待刷写完毕

![flash system](https://www.helloimg.com/i/2025/03/07/67ca2eae3f7e1.png)

等待刷写完成后

输入

`e userdata`

以清除用户数据分区，如果不清除的话可能会导致卡第一屏

输入

`reset`

以重启

## 1.5如停止响应恢复备份系统

若您的设备在启动时一直停止响应，并显示此屏幕，那您的设备可能无法使用此方法或者没有找到对的刷机包。

请使用上文的r system方法将原备份的系统刷回去就行，具体命令是： r system 盘符:您备份的文件地址\文件名。

![Error fix](https://www.helloimg.com/i/2025/03/07/67ca2fc35e7ee.png)

## c6系统注意事项

请注意，c6包的开发者密码是：IFlyCBaistudy5121

你实际上也可以下个爱玩机工具箱来直接打开adb(我个人更推荐这种)

# 2.学习机系统制作官改版系统教程

## 2.0 阅读要求

1.学习机系统底层是android9

2.熟练掌握[1.0教程](#1紫光展锐处理器部分机型深刷破解)所有内容，本教程不会顾及你的任何基础

3.本教程修改系统部分需要在Debian上进行

4.[system法root](#22-修改systemvendorroot)与[替换安装器](#23-修改system替换安装器)仅适用于零售版系统

## 2.1 文件准备

magisk安装包（26+，官版和Kitsune都行的）

由 A9版本GSI镜像/校园版官刷后版本 提取得到

boot,system,vendor镜像自己想办法得到

## 2.2 (修改system/vendor)root

linux上挂载system镜像与vendor镜像为**读写**，解压magisk安装包

我这里magisk安装包解压到了/mnt/d/m

system挂载到了/mnt/d/root

vendor挂载到了/mnt/d/vendor

电脑侧修补vendor需要的文件:

magiskinit-x86:/mnt/d/m/lib/x86_64/libmagiskinit.so

precompiled_sepolicy:/mnt/d/vendor/etc/selinux/precompiled_sepolicy

修补平板上system分区需要的文件（左边是文件名,右边是这些文件的路径）：

magisk32:/mnt/d/m/lib/armeabi-v7a/libmagisk.so

magisk64:/mnt/d/m/lib/arm64-v8a/libmagisk.so

magiskpolicy:/mnt/d/m/lib/arm64-v8a/libmagisksepolicy.so

magiskinit:/mnt/d/m/lib/arm64-v8a/libmagiskinit.so

stub.apk:就你解压的这个magisk安装包，我这里就是/mnt/d/app-debug.apk

config:使用 `echo -e "SYSTEMMODE=true\nRECOVERYMODE=false" > config`命令创建

上面这几个文件得到后，使用cp命令将几个文件移到/mnt/d/root/system/bin以及/mnt/d/root/system/etc/init/magisk

（注:bin文件夹中不该有stub.apk和config文件）

两个文件夹(magisk文件夹自行创建)，把这些文件的owner设为0，权限给700

对/mnt/d/root/system/etc/init/bootanim.rc进行复制，复制为/mnt/d/root/system/etc/init/bootanim.rc.gz

对/mnt/d/root/system/etc/init/bootanim.rc进行以下修改：添加以下内容并保存

```

on post-fs-data

    start logd

    exec u:r:su:s0 root root -- /system/etc/init/magisk/magiskpolicy --live --magisk

    exec u:r:magisk:s0 root root -- /system/etc/init/magisk/magiskpolicy --live --magisk

    exec u:r:update_engine:s0 root root -- /system/etc/init/magisk/magiskpolicy --live --magisk

    exec u:r:su:s0 root root -- /system/etc/init/magisk/magisk64 --auto-selinux --setup-sbin /system/etc/init/magisk /sbin

    exec u:r:su:s0 root root -- /sbin/magisk --auto-selinux --post-fs-data


on nonencrypted

    exec u:r:su:s0 root root -- /sbin/magisk --auto-selinux --service


on property:vold.decrypt=trigger_restart_framework

    exec u:r:su:s0 root root -- /sbin/magisk --auto-selinux --service


on property:sys.boot_completed=1

    mkdir /data/adb/magisk 755

    exec u:r:su:s0 root root -- /sbin/magisk --auto-selinux --boot-complete

    exec u:r:su:s0 root root -- /system/bin/sh -c "settings put global adb_enabled 1"

    exec u:r:su:s0 root root -- /system/bin/sh -c "setprop service.adb.tcp.port 5555"

    exec u:r:su:s0 root root -- /system/bin/sh -c "setprop ctl.restart adbd"


on property:init.svc.zygote=restarting

    exec u:r:su:s0 root root -- /sbin/magisk --auto-selinux --zygote-restart

    exec u:r:su:s0 root root -- /system/bin/sh -c "settings put global adb_enabled 1"

    exec u:r:su:s0 root root -- /system/bin/sh -c "setprop service.adb.tcp.port 5555"

    exec u:r:su:s0 root root -- /system/bin/sh -c "setprop ctl.restart adbd"

   

on property:init.svc.zygote=stopped

    exec u:r:su:s0 root root -- /sbin/magisk --auto-selinux --zygote-restart

    exec u:r:su:s0 root root -- /system/bin/sh -c "settings put global adb_enabled 1"

    exec u:r:su:s0 root root -- /system/bin/sh -c "setprop service.adb.tcp.port 5555"

    exec u:r:su:s0 root root -- /system/bin/sh -c "setprop ctl.restart adbd"

```

另使用magiskinit-x86文件进行以下操作:

```

chmod +x magiskinit-x86的文件位置

magiskinit-x86的文件位置 --patch-sepol /mnt/d/vendor/etc/selinux/precompiled_sepolicy /mnt/d/vendor/etc/selinux/precompiled_sepolicy.gz


magiskinit-x86的文件位置 --patch-sepol /mnt/d/vendor/etc/selinux/precompiled_sepolicy /mnt/d/vendor/etc/selinux/precompiled_sepolicy

```

成功Root.

## 2.3 (修改system)替换安装器

将/mnt/d/root/system/priv-app中DefcontainerService与PackageInstaller使用你得到的无限制版本进行替换。

并将替换后的/mnt/d/root/system/priv-app/DefcontainerService/lib/arm64/libdefcontainer_jni.so与/mnt/d/root/system/lib64/libdefcontainer_jni.so进行软链接(要相对路径而非绝对路径，泪的教训)，我这里使用以下命令：

```

cd /mnt/d/root/system/priv-app/DefcontainerService/lib/arm64/


rm -rf libdefcontainer_jni.so


ln -s ../../../../lib64/libdefcontainer_jni.so libdefcontainer_jni.so

```

然后就结束了

## 2.4 (修改boot)boot方法root

> Warning:Magisk方式Root具有及其高的不确定性，可能你启动完一次重启它就无法再进系统了，也可能你能一直用，非常玄学，如果你只是为了使用爱玩机（即除了那个默认模块以外什么也不用），你实际上可以只使用Apatch的，作为Root权限管理器而言Apatch方法更稳定

### 2.4.1 (修改boot)Apatch法

电脑方法：参考[APatch 安装指南 | APatch Docs](https://apatch.dev/zh_CN/install.html#%E8%87%AA%E5%8A%A8%E4%BF%AE%E8%A1%A5)以及[在线修补](https://kernelpatch-on-web.pages.dev/)
得到了修补好的镜像以后，去Fork [这个仓库](https://github.com/TomKing062/action_big_resign_with_magisk)并进入你Fork的仓库-Actions（会有一个警告，自己看。你点击绿色的就可以启用这个仓库的Actions功能了）
![功能介绍](image/Unisoc/1742742807689.png)
这里Apatch修补要用的是第二个，点进 `sign-one-partition-only`，输入好镜像直链地址，第二个空是填写分区名称的，这里是boot，然后再点 `Run Workflow`(文件自己想办法或者参考下面那一部分把文件上传Github的步骤)，即可在几分钟后在本仓库Releases下找到修补好的镜像文件，名称为image.img(Tips:记得看文件大小，小的不自然就说明链接错了，重新获取直链再重新跑)

### 2.4.2 (修改boot)Magisk法

首先确保你有一个Github账户，没有可以去GitHub.com首页右上角自行注册一个以备用

在登录好的默认界面中，你需要打开这个链接[ New](https://github.com/new)，Repository name填写为任意名称，点击下方的绿色按钮以创建

创建好后，自行下载GithubDesktop并登录Github账号（可参考[安装 GitHub Desktop 并进行身份验证 - GitHub 文档](https://docs.github.com/zh/desktop/installing-and-authenticating-to-github-desktop)）

在你的Github Desktop中打开 `Files(F)`并打开对应着 `Ctrl+Shift+O`快捷键的那个选项，从里面找到你刚建的仓库，双击并等待Clone完成

使用spd_dump从设备中将splloader,uboot,sml,trustos,vbmeta,boot与recovery分区提出来并打包为一个zip格式的压缩包（必须确保每个分区镜像后缀名为.bin），并将该压缩包放入GithubDesktop Clone到的那个仓库内部，放完后回到GithubDesktop里面，它应该会显示更改，你Commit并Pull即可

后面的步骤相对简单些，你需要Fork [这个仓库](https://github.com/TomKing062/action_big_resign_with_magisk)并进入你Fork的仓库-Actions（会有一个警告，自己看。你点击绿色的就可以启用这个仓库的Actions功能了）
![功能介绍](image/Unisoc/1742742807689.png)
这里Magisk修补要用的是 `resign`方法，点击进入再点 `Run Workflow`，把你上传到仓库的压缩包的直链链接获取了复制进去并运行即可在几分钟后该仓库的Releases里面找到它修补并签名好的镜像压缩包 `output.zip`，解压后就能找到修补好的boot镜像并刷入了，教程结束

## 2.5 (仅修改system) 获得一个精简的类似GSI的system分区
