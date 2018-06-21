


> 积累生命壹号平时遇到的MacTips。



### 001 Mac到底要不要关机

对于关机，我的观点是：

- 如果每天用，建议 Mac 不关机，使用睡眠模式；
- 如果不常用，建议 Mac 关机。

具体可以看这篇文章：[Mac 到底要不要关机？| 领客专栏 · MacTips](http://www.ifanr.com/app/657745)




### 002 重置 SMC

如果发现 Macbook Pro 的某一个 Type-C 失效了，能充电，但是 HDMI 和 USB 网络都不行，此时可以重置 SMC。

重置  SMC 是个 Mac 常用操作，电源、背光、亮屏、不能充电等等，都可以以此解决，不过很多人不知道。如何 重置 SMC 呢？

1、将 Mac 关机。
2、在内建键盘上，按下键盘左侧的 Shift-Control-Option 键，然后同时按下电源按钮。按住这些按键和电源按钮 10 秒钟。
如果您的 MacBook Pro 带有 Touch ID，则 Touch ID 按钮也是电源按钮。
3、松开所有按键。
4、再次按下电源按钮以开启 Mac。



### 003 卸载软件后，清除残留

虽然程序已经被删除了，但硬盘上可能会有残留文件。这些文件占内存小，如果你之后重新安装该应用程序的话，它们是会保留的。但如果以后再也不用的话，可以选择彻底删除。


步骤如下：

（1）打开资源库Library：按住⌥ Option键，单击“前往”菜单，菜单下就会出现“资源库”选项。
（2）删除缓存：在`Application Support`（应用程序支持）目录里，删除对应软件的文件夹。
（3）删除偏好设置：在`Preferences`（偏好设置）目录里，删掉对应软件的偏好设置文件。


温馨提示：

在终端输入命令`chflags nohidden ~/Library`，可以永久显示资源库Library文件夹。

参考链接：

- [wikiHow](https://zh.wikihow.com/%E5%9C%A8Mac%E4%B8%8A%E5%8D%B8%E8%BD%BD%E7%A8%8B%E5%BA%8F)



### 004 Mac 备份微信聊天记录的问题（20180218）

问题描述：MAC版微信可以备份手机聊天记录到电脑了，但是手机和电脑明明是在同一个网络了，却说不在。手机显示的是网络名称，电脑的网络显示的是***的macbook。

解决：把电脑里“设置-共享”里面的名称改为Wi-Fi的名称，就可以备份。

PS：网上都是这个答案，但是我自己试了一下，还是不行。


### 005 电脑锁屏（20180220）

问题描述：把电脑合上以后（或者按 Touch Bar上的锁定键后），再立即打开电脑，发现电脑并没有锁屏。原因是需要设置锁屏的时间。

解决：「系统偏好设置 -->安全与隐私 --> 通用 --> 进入睡眠或开始屏幕保护程序 --> 选择“立即”」。



### 006 修改host文件


点击 Finder，在顶部菜单栏选择“前往”－“前往文件夹”，粘入 `/private/etc/` 这个路径（不带引号），找到`hosts`文件。


### 007 iPad上取消爱奇艺会员的续费

![](http://img.smyhvae.com/20180426_2338.png)


### Android手机连接Mac


### 009 将 iMac 作为 MacBook pro 的外接显示器

首先一定要看官方文档：[通过目标显示器模式将 iMac 用作显示器](https://support.apple.com/zh-cn/ht204592)


我的MacBook pro是最新款的，接口全是type c的。如下：

![](http://img.smyhvae.com/20180621_1300.png)


我的 iMac 是2013年款的，接口是Thunderbolt 2。如下：

![](http://img.smyhvae.com/20180621_1305.png)



所以，为了能让 iMac 接上 MacBook pro，必须要买转接线，而且要买苹果官方提供的转接线：

- [雷雳 3 (USB-C) 转雷雳 2 转换器 | 384元](https://www.apple.com/cn/shop/product/MMEL2FE/A)

- [Thunderbolt 2连接线 (2.0 米) | 285元](https://www.apple.com/cn/shop/product/MD861FE/A)

注意，Thunderbolt 2和 Mini DisplayPort是有区别的，虽然二者的接口外形是相同的，但前者比后者更高端。


转接线买回来之后，就按照官方文档提供的步骤来操作吧。步骤如下。

请按照以下步骤操作，以开始将 iMac 用作显示器：

- （1）确保您的 iMac 已开机，并确保另一台 Mac 已登录到 macOS 用户帐户。

- （2）在两台电脑之间连接 Mini DisplayPort 或 Thunderbolt 连接线。

- （3）在要用作显示器的 iMac 的键盘上按下 「Command + F2」。

注意，按下 「Command + F2」 后，iMac 才会作为 MacBook pro的扩展桌面。**一定要按这个按键，否则的话，是不生效的**。

**iMac的外接键盘的问题**：

我的iMac是外接的苹果官方提供的无线蓝牙键盘，按下 「Command + F2」之后，是可以生效的。

但是，普通的键盘按下「Command + F2」，却不会生效。要怎么解决这个问题呢？有两种方法：

方法1：普通键盘按「fn + Command + F2」。这个方法我没试过，因为必须要提供带有fn的普通键盘。

方法2：安装软件[KeyRemap4MacBook](https://pqrs.org/osx/karabiner/)，将`F2`键重新映射为`display_brightness_increment`。如下：

![](http://img.smyhvae.com/20180621_1310.png)

**方法2亲测有效**。我是看了[小试 iMac TDM 模式](http://blog.lanvige.com/2014/02/13/try-imac-tdm-mode/)这篇文章才知道的。也是从这篇文章得知，iMac作为外接显示器，这种模式叫做 **TDM（Target Display Mode）模式**。

另外，还有一篇文章比较有意思，可以看看：[使用第三方键盘激活iMac TDM？没门儿！](https://www.yilan.io/article/56963cbdc609c2a7142a91d4)








