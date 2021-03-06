---
title: "我的 ITX Hackintosh / PC 购买、组装、安装系统心得"
date: 2019-07-11T11:50:00+08:00
toc: true
# images:
tags: 
  - things
  - mac
  - hackintosh
  - pc
  - itx
---

## 前言

一直以来缺少一台自己的有一定性能的台式机，从五月份开始思考需求，到处爬楼，多次增删，得到以下结果，仅以记之。

## 需求

- ITX台式机
- 甜品级性能
- 较久的使用寿命，极少的更换、升级、维修可能，未来直接配新的电脑
- Hackintosh
- Windows
- 很少大于3A的游戏需求
- 尽量无光污染

## 配置单

| 类别         | 名称                                                                                               | 价格 | 平台 |
| -------------- | ---------------------------------------------------------------------------------------------------- | ---- | ---- |
| CPU            | 英特尔i7 8700散片                                                                               | 1789 | 淘宝 |
| 主板         | 玩家国度（REPUBLIC OF GAMERS）ROG STRIX Z390-I GAMING 主板（Intel Z390/LGA 1151）          | 1809 | 京东 |
| 显卡         | 蓝宝石（Sapphire）RX590 8G D5 超白金极光特别版1545-1560MHz/8000-8400MHz 8GB/256bit GDDR5 DX12显卡 | 1399 | 京东 |
| 内存         | 美商海盗船(USCORSAIR)DDR4 3200 16GBX2 台式机内存条 复仇者LPX系列 游戏型           | 1078 | 京东 |
| 散热         | 美商海盗船 (USCORSAIR) H100i PRO RGB冷头 一体式CPU水冷散热器 （240MM冷排/2×120磁悬浮风扇/五年质保） | 748  | 京东 |
| 电源         | 【SGPC】海盗船SF600/SF750全模组A4迷你ITX小机箱SFX小电源600w+模组线                | 799  | 淘宝 |
| macOS系统盘 | WD西部数据 SN750 黑盘 500G PCI-E M.2 NVME固态硬盘SSD                                       | 539  | 淘宝 |
| Windows系统盘 | WD西部数据 SN750 黑盘 500G PCI-E M.2 NVME固态硬盘SSD                                       | 539  | 淘宝 |
| 机箱         | SKTC游戏机箱itx机箱电脑机箱台式全铝钢化玻璃机箱240水冷机箱S02 红色单钢化玻璃（含PCIE延长线） | 517  | 京东 |
| Wi-Fi和蓝牙 | 博通BCM94352Z 戴尔DW1560 802.11AC无线网卡 ngff接口 黑苹果                              | 278   | 淘宝 |
| 显示器（已有） | Dell U2417H                                                                                          | 0    |      |
| 显示器 | LG 27UL850                                                                                          | 3500    |   淘宝   |
| DP线          | 绿联（UGREEN）DP高清线1.2版 2K*4KDisplayPort公对公接线 笔记本电脑连接显示器视频线支持戴尔1.5米 10245 | 45   | 京东 |
| 总计         |                                                                                                      | 9540 |      |

>> 趁着618入手的，表格实际总计是9300左右（退货的DW1820A是70左右）

>> 双十一入手LG 27UL850，4K对Mac的显示提升挺大的，真香！不需要USB-C、HDR、扬声器，可以考虑更便宜的。

## 为什么这么选

### CPU

我的CPU选择标准/理由：

- 适合Hackintosh，目前Intel更方便
- ITX散热性能较差，不超频
- 少于2000元的预算，感觉超过2000元的产品价格和能耗都提升了一个档次

本来选择的是i5-9600K，但是根据朋友建议和[这个对比](https://cpu.userbenchmark.com/Compare/Intel-Core-i7-8700-vs-Intel-Core-i5-9600K/3940vs4031)，放弃10%左右的单核性能提升，选择无超频、低TDP、多核多线程更强的i7-8700。两者差别其实不是很大，可以根据价格决定。

### 主板

选择ROG STRIX Z390-I是因为：

- Z370和Z390系列较新，且适合Hackintosh，DP/HDMI/DVI核显输出黑屏概率低
- 需要ITX版型
- tonymacx86中的大部分新帖子都是Z390，适合参考
- 相比华擎同款，没有我不需要的PS/2接口、半速Thunderbolt接口，且自带Wi-Fi天线

缺点是性价比低，海淘性价比较高，但无保修。

>> 主板周围灯光可以在BIOS中关闭

>> 使用至今（19年11月）的一些小问题：虽然新帖子是Z390，但大部分不是ROG Z390-I，略有不同；我没有好的螺丝刀，拆装容易滑丝

### 显卡

- Nvdia显卡不易驱动，考虑AMD，macOS可以直接驱动RX590
- 蓝宝石适合Hackintosh，稳定
- 不那么高的性能需求
- Vega56价格、能耗高，ITX机箱限制

>> 蓝宝石的软件支持较差，蓝色风扇灯光无法关闭

### 内存

- 降价非常明显，尽量一步到位（2x16GB）
- 不需要灯光
- 3200MHz和其他频率的产品价格差别不大
- 尽量套条

### 散热

ITX机箱对风冷限高比较严格，找来找去没有发现特别适合的方案，又发现SKTC S02这款机箱支持240一体式水冷，于是考虑使用水冷。不需要光，京东按销量排序，选中了这款，虽然有点贵，但有5年质保和2400RPM的风扇转速和75CFM的风量，压制i5-9600K或i7-8700应该都可以。

>> 灯光在Windows下可以完全关闭，在macOS下会是默认的循环渐变色，Windows下关闭后，Mac定制好USB，睡眠时会关闭灯光

### 电源

- ITX机箱要求SFX
- 显卡推荐电源600W以上

京东按上面条件搜索，比较合适的就是海盗船这款和EVGA的一款，爬楼时发现大量ITX装机都使用海盗船这款，在淘宝某家店发现带定制线还比京东更便宜（~~SF600的原装线非常硬~~实际个人感觉不是很硬）。

### 硬盘

- 双系统，双硬盘，不分区
- macOS主要是日常使用，Windows主要是游戏，各500GB应该可以满足我的需求
- 由上面两条，不需要机械硬盘

根据下图和Hackintosh硬件推荐，SN750应该是近期性价比最高（淘宝）的NVMe SSD。

![SSD对比](https://spider.ws.126.net/5c1b0b595fff3e8a61bf0fc454bde3d1.jpeg)

### 机箱

机箱来回挑选了很久，大概的需求是：

- 能放下显卡
- 只需要ITX版型
- 只需要SFX大小的电源
- 散热、做工不错

这样得出的结果大致是10升的A4机箱，需要显卡转接线，市面上有许多产品。

国外论坛上的SFF Build帖子大多是用Ghost S1、Dan Case之类的A4机箱，但这些需要转运并且特别贵。也有老外在淘宝买然后转运出去的。然后自己在淘宝搜也是一头雾水。B站up主 @玩笑笑笑笑笑 的视频[[B站最详细]ITX装机指南(收录25款散热器&98款机箱)](https://www.bilibili.com/video/av51769793)使我对ITX机箱有了比较清晰的认识，大致对比了一下选择了SKTC S02这款，红色的颜值还是挺舒服的。

没有选择比较热门的水冷快乐盒、小方糖等A4机箱是因为这些款式加上显卡转接线价格也不低，有的要写文章发帖子才能减免。另外看描述SKTC S02的金属壳体是比较厚的。

实际使用中没什么大任务运行也有稍温暖的风散出，LOL全特效运行有时会有呼呼的风。

另外一提，银河W1非常好看，适合经济宽裕动手能力强的人入手。

### Wi-Fi和蓝牙卡

Wi-Fi、蓝牙、Handoff和Airdrop功能需要合适的无线网卡，根据[这个列表](https://osxlatitude.com/forums/topic/11138-inventory-of-supportedunsupported-wireless-cards-2-sierra-catalina/)和[这个帖子](https://www.tonymacx86.com/threads/the-everything-works-asus-z390-i-gaming-i7-8700k-sapphire-rx580-pulse-build.272572/)，ROG STRIX Z390-I这块主板可以把M.2 Intel网卡替换成DW1560，但淘宝的DW1560溢价太严重，有的还断货，根据[这个帖子](https://osxlatitude.com/forums/topic/11322-broadcom-bcm4350-cards-under-high-sierramojave/)，DW1820A某些型号也是可以的，需要额外驱动，淘宝的售价是DW1560的五分之一。

尝试DW1820A后发现此卡非常不稳定，会出现卡顿、无法连接的现象，尝试了多种驱动方式也无效。根据帖子的信息，贴纸上标记的料号似乎也不符合软件查看的`subsystem-id`，怀疑店家贴了标签，遂退货，入手278元的DW1560，十分稳定。

## 组装

第一次组装ITX，实在非常困难，螺丝、组件、线材、机箱都非常小，排列紧凑。

建议使用DP接口以避免图形问题。

对于这些零件（机箱、主板、水冷、电源、显卡）的配合，我建议的安装顺序是：

- 打开机箱侧面和上面外壳
- 安装主板背部水冷支架
- 插入内存
- 更换DW1560
- 安装电源，我使用的是风扇向里，插头朝下的方式
- 安装显卡：显卡延长线从显卡底部连接，180度弯折绕到显卡背部和中板之间，伸到顶部，180度弯折绕过中板顶部以连接到主板，插入8+6pin电源，注意电源线和第二次弯折的显卡延长线不能太高，否则可能碰到冷排风扇
- 合上显卡侧机箱外壳
- 安装风扇到冷排，安装冷排到机箱，合上机箱上外壳
- 安装主板、水冷头、剩余接线。此时要注意走线，我的做法是把风扇线、水冷管、机箱USB3线、电源按钮跳线等需要绕的线都塞在电源、主板、中板间的区域；把电源按钮跳线、水冷头USB2线穿过显卡延长线再接
- 合上主板侧机箱外壳

### 更换DW1560流程（来自tonymacx86帖子）

卸下主板背部固定灰色马甲的4个黑色螺丝。取下散热器并放在一边

![MB Screws.jpg](https://images-1251731554.file.myqcloud.com/DW1560-MB%20Screws.jpg)

卸下主板背部固定WiFi模块的2个银色螺丝
将固定IO挡板的弹簧夹掰开取下，别担心，它的铰链结构不会弯曲

![Clip.jpg](https://images-1251731554.file.myqcloud.com/DW1560-Clip.jpg)

将IO挡板取下，小心地将M.2 Wi-Fi模块向上拉出

![Module.jpg](https://images-1251731554.file.myqcloud.com/DW1560-Module.jpg)

卸下模块侧面固定螺丝

![Sidescrew.jpg](https://images-1251731554.file.myqcloud.com/DW1560-Sidescrew.jpg)

向上滑动前盖并将其完全取下，您可能需要稍微拆下后贴纸

![Cover.jpg](https://images-1251731554.file.myqcloud.com/DW1560-Cover.jpg)

小心卸下两条天线，上面的天线连接的是左边的接口

![board.jpg](https://images-1251731554.file.myqcloud.com/DW1560-board.jpg)

拧开固定螺丝，取下旧模块，小心不要撕破小海绵垫片，换上新模块并装上螺丝
小心连接天线，连接头不好安装，确保它们咔哒一声到位，不要太大力，以免压碎它们
反向重复该过程，装回主板。

### 最终成果

![IMG_0177.jpg](https://images-1251731554.file.myqcloud.com/IMG_0177.jpg)

![IMG_0178.jpg](https://images-1251731554.file.myqcloud.com/IMG_0178.jpg)

![IMG_0179.jpg](https://images-1251731554.file.myqcloud.com/IMG_0179.jpg)

![IMG_0180.jpg](https://images-1251731554.file.myqcloud.com/IMG_0180.jpg)

![IMG_0181.jpg](https://images-1251731554.file.myqcloud.com/IMG_0181.jpg)

## Hackintosh安装

主要参考了[The everything works Asus Z390-I Gaming * i7-8700K * Sapphire RX580 Pulse build| tonymacx86.com](https://www.tonymacx86.com/threads/the-everything-works-asus-z390-i-gaming-i7-8700k-sapphire-rx580-pulse-build.272572/)这个帖子。

### 前置准备

- 一台可用的Mac（使用Windows PC的话需要参考网上其他教程，配置iCloud的部分可能要在Hackintosh上做）
- 一个8GB或更大的U盘
- 待安装的Hackintosh机器
- 下载，解压缩，安装[Clover Configurator](https://mackie100projects.altervista.org/download/ccg/)。在制作安装U盘过程中用来配置iCloud等，在安装完成后用来在Hackintosh上挂载EFI分区，所以在Mac和待安装的Hackintosh机器上都要安装

### 制作安装U盘

>> 也可以使用Etcher

- 在Mac中插入8GB或更大的U盘
- 打开`/Applications/Utilities/Disk Utility.app`并在左侧面板中选择U盘
- 点击“抹掉”按钮
- 命名U盘，可以稍后重命名
- 格式：选择OS X Extended（Journaled）
- Scheme：选择GUID Partition Map
- 单击“擦除”然后“完成”
- 下载[Unibast for Mojave](https://www.tonymacx86.com/resources/unibeast-9-2-0-mojave.426/download)
- 从应用商店下载Mojave安装程序
- 运行UniBeast并选择U盘，Mojave安装程序和UEFI。将其他所有内容留空，然后单击继续以创建安装程序。这可能需要很长时间，所以要耐心等待
- 下载[我的EFI](https://github.com/ladit/hackintosh/tree/master/EFI)并替换U盘EFI分区中的EFI文件夹，双击使用Clover Configurator打开U盘EFI分区下的`/EFI/CLOVER/config.plist`
- 单击Clover Configurator 左侧的SMBIOS
- 单击System下的Serial Number右侧的Generate New
- 点击右侧iMac图片下的Check Coverage
- 你将被带到苹果网站，输入验证码，如果出现以下消息，说明序列号是有效的，否则重新Generate New

>> 很抱歉，此序列号无效。请检查您的信息，然后再试一次。

- 一旦你得到一个有效的序列号，点击SmUUID右侧的Generate New，将iMac图片左侧的Board Serial Number复制到左边Rt Variables中的MLB栏，点击左下角第二个按钮保存配置，弹出U盘

### BIOS设置

- 开机，按Delete进入BIOS
- 更新BIOS
- 将BIOS恢复到默认设置
- 在左侧主屏幕中，将XMP设置为“enabled”
- Advanced Items > CPU Configuration > Intel (VMX) Virtualization Technology > Enable - 打开虚拟化支持
- Advanced Items > System Agent (SA) Graphics Configuration > Primary Display > PEG (如果使用集显，设为auto)
- Advanced Items > System Agent (SA) Graphics Configuration > IGPU Multi-Monitor > 独显：Enabled，集显：Disabled
- 保存并重启到BIOS
- Advanced Items > System Agent (SA) Graphics Configuration > RC6(Render Standby) > Off
- Advanced Items > System Agent (SA) Configuration > Above 4G Decoding > Enable
- Advanced Items > System Agent (SA) Graphics Configuration > DVMT Pre-Allocated > 128M
- Advanced Items > USB Configuration > Legacy USB Support > Disabled
- Advanced Items > USB Configuration > XHCI Hand Off > Enabled
- 保存并重启

一些其他可选设置：

Boot> Boot Configuration> Boot Logo Display> Disabled
Boot> Boot Configuration> Post Report> 1 Sec
Boot > Setup Mode > Advanced

保存BIOS设置为模板：

Tools > Asus User Profile > Profile Name > Mac
Tools > Asus User Profile > Save to Profile > 1

### 安装系统

- 将安装U盘插入待安装的机器，从Clover菜单中启动并选择Installer作为启动盘，安装系统，过程中将多次重启，在Clover中选择从本地磁盘启动就可以继续。建议进入系统后再登录iCloud
- 下载，解压缩，安装[Clover Configurator](https://mackie100projects.altervista.org/download/ccg/)
- 单击工具下的Mount EFI，挂载U盘和本地磁盘的EFI分区，用U盘的EFI文件夹替换本地磁盘的EFI文件夹（若制作启动U盘时没有生成SMBIOS等操作，在此时对本地磁盘下的clover.plist生成）
- 下载并启动Hackintool，在电源Tab下点击小齿轮修复休眠
- 下载[Kext Utility](http://cvad-mac.narod.ru/index/0-4)并运行，修复权限与缓存，直到显示`All done`，右下角按钮变为`quit`，退出
- 重新启动进入BIOS，设置本地磁盘为第一引导顺序
- 启动并检查以下项目是否正常运行：

- Continuity:
  - Handoff
  - iMessage
  - Continuity Camera
  - Universal Clipboard
  - Instant Hotspot
  - Air Drop
  - iPhone Cellular Calls
  - Auto Unlock
  - Apple Pay​
- Sleep (fans and RGB LEDs included)
- Power Nap (sleep with background operations such as Time Machine)
- Wake
- CPU frequency tuning
- H264/HEVC hardware encoding and decoding
- Audio (select internal speakers)
- Ethernet
- Bluetooth
- WiFi
- All USB and USB 3.1 ports
- Function keys(such as brightness or volume)
- Nightshift (no kexts required)

### 成果

完美运行：

- Continuity:
  - Handoff
  - iMessage
  - Continuity Camera
  - Universal Clipboard
  - Instant Hotspot
  - Air Drop
  - iPhone Cellular Calls
- Sleep (fans and RGB LEDs included)
- Wake
- CPU frequency tuning
- H264/HEVC hardware encoding and decoding
- Audio (select internal speakers)
- Ethernet
- Bluetooth
- WiFi
- All USB and USB 3.1 ports
- Nightshift (no kexts required)

存在问题：

- ~~Function keys(such as brightness or volume)：外接显示器无法调节，但我的IKBC G104按住fn键+F9-F11可以调节音量~~，使用Karbiner-Elements应该可以实现这个功能

无效：

- Apple Pay​：无硬件

未测试：

- Power Nap (sleep with background operations such as Time Machine)：未确认，猜测可以，因为睡眠后散热器灯有时会亮起，应该是自动唤醒，过一会儿会继续睡眠
- Auto Unlock（应该可行）
- USB 3.1 Gen 2 port：连接27UL850的Type-C后能把键鼠接在显示器上，各个高速USB口连接时显示的似乎都是5Gbps的速度，猜测可以支持

## Windows安装

使用另一个U盘刷入PE，装在另一块硬盘即可，Clover会自动检查到启动项。

## 后记

使用了一段时间，从个人需求来看，CPU、显卡、散热、电源都有点性能过剩。

Hackintosh的使用遇到了很大的阻碍，先是DW1820A很不稳定，时不时断网，换了DW1560后稳定许多。

但总是出现**随机自动断电重启**的现象（参考的帖子应该是旧的BIOS和macOS版本，但帖子里的回复也没有提到这个问题的），`log show --predicate 'eventMessage contains "Previous shutdown cause"' --last 24h`命令显示历史的重启都是正常的。log没有显示kernel panic的原因应该是
Z390无法支持NVRAM，只能模拟，崩溃后不能记录下来错误。重启找遍Google和tonymacx86没有结果。有的说要定制USB，但我定制后似乎还是会出现这个问题。经过多次测试，~~应该可以确认是BIOS里某个电源管理相关的选项导致此问题~~，几个月的崩溃后注意到每次断电重启时都是在发起一次网络连接（一般是点击一个超链接），怀疑是网卡驱动的问题，而我当时已经手动关闭Wi-Fi很久了，问题应该出在有线网卡，找到IntelMausiEthernet作者的[帖子](https://www.insanelymac.com/forum/topic/304235-intelmausiethernetkext-for-intel-onboard-lan/)，关于kp建议清除和重建缓存，联想到我安装系统后也升级过几次，看起来没有问题，可能实际这就是导致重启的原因。另外EFI的原作者使用的IntelMausiEthernet竟然还是beta版本的，我注册了insanelymac并下载了最新版，如今确实已经稳定使用了很久，可以说几乎完美。

tips：定制USB驱动可以获得更好的睡眠效果，可以参考下方的参考链接。

## 参考

- [使用Hackintool定制黑苹果USB驱动](https://sleele.com/2019/06/07/%E4%BD%BF%E7%94%A8hackintool%E5%AE%9A%E5%88%B6%E9%BB%91%E8%8B%B9%E6%9E%9Cusb%E9%A9%B1%E5%8A%A8/)
- [【2019年6月】6月份装机走向与推荐](https://zhuanlan.zhihu.com/p/67807395)
- [macOS Mojave 台式机黑苹果硬件选购指南-远景论坛-微软极客社区](http://bbs.pcbeta.com/viewthread-1799271-1-1.html)
- [The everything works Asus Z390-I Gaming * i7-8700K * Sapphire RX580 Pulse build| tonymacx86.com](https://www.tonymacx86.com/threads/the-everything-works-asus-z390-i-gaming-i7-8700k-sapphire-rx580-pulse-build.272572/)
- [攒了一台 4K 视频剪辑黑苹果 · icyleaf](http://icyleaf.com/2019/01/itx-coffee-lake-hackintosh-build-for-4k-video-editing/)
- [华擎 Z390 Gaming ITX 黑苹果安装教程 · icyleaf](http://icyleaf.com/2019/03/asrock-z390-gaming-itx-install-hackintosh-tutorial/)
- [黑苹果安装系统教程](http://www.oadun.com/2018/12/215.html)
- [使用Hackintool定制黑苹果USB驱动](https://sleele.com/2019/06/07/%E4%BD%BF%E7%94%A8hackintool%E5%AE%9A%E5%88%B6%E9%BB%91%E8%8B%B9%E6%9E%9Cusb%E9%A9%B1%E5%8A%A8/)
- [Broadcom BCM4350 cards under High Sierra/Mojave - Wireless and Bluetooth - osxlatitude.com](https://osxlatitude.com/forums/topic/11322-broadcom-bcm4350-cards-under-high-sierramojave/)
- [tonymacx86](https://www.tonymacx86.com/)
- [黑果小兵的部落阁](https://blog.daliansky.net/)
