## 将 iMac 作为 MacBook pro 的外接显示器（扩展显示器）

### 参考文档


首先一定要看官方文档：

- [通过目标显示器模式将 iMac 用作显示器](https://support.apple.com/zh-cn/ht204592)

- [MacBook pro 2016 使用 iMac2013末 21寸作为外接显示器](https://discussionschinese.apple.com/thread/140129694)

绿联网站也有详细的文档：

- [苹果iMac如何用作显示器，成为MacBook扩展屏](https://www.lulian.cn/news/149-cn.html)

### 设备需要满足的条件

设备需要满足以下条件，才能让 iMac作为 MacBook 的扩展显示屏：（这个是我咨询苹果官方客服后，得到的答案）

- iMac必须是老款的；且系统版本必须是 10.13.6 或更低版本。

- MacBook必须是2019年款或更老的版本；且系统版本必须是 10.15 或更低版本。

![](https://img.smyhvae.com/20220818-0930.png)

我的MacBook pro是 2016年款（带了 touch bar），接口全是 type c 的。如下：

![](https://img.smyhvae.com/20180621_1300.png)

我的 iMac 是2013年款的，接口是 Thunderbolt 2。如下：

![](https://img.smyhvae.com/20180621_1305.png)

### 转接线

为了能让 iMac 接上 MacBook pro，必须要买转接线，而且要买苹果官方提供的转接线：

- [雷雳 3 (USB-C) 转雷雳 2 转换器 | 384元](https://www.apple.com/cn/shop/product/MMEL2FE/A)

- [Thunderbolt 2连接线 (2.0 米) | 285元](https://www.apple.com/cn/shop/product/MD861FE/A)

注意，Thunderbolt 2 和 Mini DisplayPort是有区别的，虽然二者的接口外形是相同的，但前者比后者更高端，二选一即可。

### 操作步骤

转接线买回来之后，就按照[官方文档](https://support.apple.com/zh-cn/ht204592)的步骤来操作吧。步骤如下。

请按照以下步骤操作，以开始将 iMac 用作显示器：

- （1）确保您的 iMac 已开机，并确保另一台 Mac 已登录到 macOS 用户帐户。

- （2）在两台电脑之间连接 Mini DisplayPort 或 Thunderbolt 连接线。

- （3）在要用作显示器的 iMac 的键盘上按下 「Command + F2」。

注意，按下 「Command + F2」 后，iMac 才会作为 MacBook pro的扩展桌面。**一定要按这个按键，否则的话，是不生效的**。

### iMac的外接键盘的问题

我的iMac是外接的苹果官方提供的无线蓝牙键盘，按下 「Command + F2」之后，是可以生效的。

但是，普通的键盘按下「Command + F2」，却不会生效。要怎么解决这个问题呢？有两种方法：

方法1：普通键盘按「fn + Command + F2」。这个方法我没试过，因为必须要提供带有fn的普通键盘。

方法2：安装软件[KeyRemap4MacBook](https://pqrs.org/osx/karabiner/)，将`F2`键重新映射为`display_brightness_increment`。如下：

![](https://img.smyhvae.com/20180621_1310.png)

**方法2亲测有效**。我是看了[小试 iMac TDM 模式](http://blog.lanvige.com/2014/02/13/try-imac-tdm-mode/)这篇文章才知道的。也是从这篇文章得知，iMac作为外接显示器，这种模式叫做 **TDM（Target Display Mode）模式**。

另外，还有一篇文章比较有意思，可以看看：[使用第三方键盘激活iMac TDM？没门儿！](https://www.yilan.io/article/56963cbdc609c2a7142a91d4)

(呵呵，上面两个连接都失效了)

