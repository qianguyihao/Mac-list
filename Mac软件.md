
> 列举mac上必装的软件



## 常用软件

### Alfred

全局搜索工具。Mac 必备工作流神器，可用它来代替系统默认的 Spotlight 搜索功能，配合上付费版的 Powerpack 之后，可以在一个输入框内完成 计算、文件搜索、网页搜索、应用程序搜索、任意脚本程序执行、任意快捷键执行自定义复杂交互。
官网链接：<https://www.alfredapp.com>




### 截图工具：截图(Jietu)


- 软件的名字就叫截图。官网下载地址：[ https://itunes.apple.com/cn/app/jie-tu-jietu/id1059334054?mt=12 ][1]

参考链接：

- [[v2ex]Mac OSX 系统上最好用的截图软件-截图（ Jietu）](https://www.v2ex.com/t/280552)

- [[少数派]试试腾讯出品的免费 Mac 截图软件：截图 Jietu](http://sspai.com/33021)



### ShadowSocks

翻墙方案1。全平台。


### Surge

翻墙方案2。Surge 是工具，不是链路。付费软件，很贵。官网下载地址：[http://nssurge.com/][3]。

推荐链路：[AgentWho](https://agentwho.network)



参考链接：

- [Surge for Mac，快捷如风](http://mp.weixin.qq.com/s?__biz=MjM5ODQ2MDIyMA==&mid=2650712713&idx=1&sn=266a2958ff395be698500febadff5e57&chksm=bec064da89b7edcccaa2f69885a564bc2153f58aa01a8829b6092851cf095f5dda26e8c44898&mpshare=1&scene=1&srcid=1117o9mBi85d6ZRijd1yMwe2#wechat_redirect)


- [mac上的surge配置](http://sining-liu-blog.logdown.com/posts/983010)

### dropbox


网盘。


### Sublime Text

最酷炫的纯文本编辑器。全平台。



### 1Password

密码管理。很贵的付费软件。全平台。官网链接：<https://agilebits.com/downloads>

我是在Mac App Store 购买的。官网购买需要64.99美元（447.6056人民币），App Store购买需要需要418人民币。



### OmniFocus

GTD时间管理软件。付费软件。Mac版：标准版39.99美元，pro版79.99美元。

如果你不是GTD的重度用户，建议不要购买这款软件，可以用其他简单的todo list类软件（如滴答清单、奇妙清单等）代替。

软件的使用可以看[少数派](http://sspai.com/tag/OmniFocus)网站的介绍。





## Markdown 软件

### Ulysses

为写作而生。很贵的软件，我在App Store买的时候，花了283元。如果你是写作的重度用户，那么推荐购买。官网链接：


### MacDown

官网链接：<http://macdown.uranusjr.com/>





### 一些常见软件

> 列举一些全平台的常见软件，这些软件也是必须要安装的。


- chrome浏览器

尽管Mac下的Safari浏览器很好用，但是chrome浏览器也是必须要用的。

官网离线下载地址：\<[https://www.google.com/chrome/browser/thankyou.html?standalone=1&platform=mac&installdataindex=defaultbrowser\#][5]\>

参考链接：
- [ 2016最新谷歌浏览器Chrome官方离线安装包下载 Win/Mac版 ][6]


- evernote印象笔记

知识管理和总结的软件。国内的类似软件有：为知笔记。

- 迅雷

- QQ & 微信

- 网易云音乐



- 欧陆词典


## 开发相关




### Xcode

苹果官网推出的IDE，程序猿必备。从App Store 上下载安装即可。




### Git安装

在App Store下载安装Xcode后，会自动安装上Git。安装好之后，在终端输入`git --version`进行验证。


### jdk

jdk  1.7下载地址：<http://www.oracle.com/technetwork/cn/java/javase/downloads/jdk7-downloads-1880260.html>


打开下载的DMG文件，双击包中的PKG文件进行安装。打开<终端>，输入 java -version，查看安装版本。

最新安装的1.7的JDK的默认安装目录为：`/Library/Java/JavaVirtualMachines`。

系统自带的JDK在以下路径中：`/System/Libray/Frameworks/JavaVM.Framwork/`，在这个目录下有个Versions目录，里面有不同版本的jdk。

我在Android Studio 中设置JDK路径的时候，默认出现了下面这个路径：

img2016112401.png

那就选择默认的这个吧，如果我手动指定jdk的路径，会报错：`[please use jdk8 or newer](http://stackoverflow.com/questions/37335214/android-studio-2-2-preview-1-error-please-use-jdk-8-or-newer)`。如下图所示：

img2016112402.png



参考链接：

- [Mac OS X 中安装JDK 7](http://www.cnblogs.com/weiok/p/4917522.html)


- [Mac设置指南](https://www.kancloud.cn/kancloud/ocds-guide-to-setting-up-mac/71035)


- [mac下卸载jdk](http://www.jianshu.com/p/8de3c3443ab4)


### Android SDK 中adb的环境变量配置

```bash
cd ~ //进入用户的根目录
touch .bash_profile // 如果没有，则新建文件；如果有，则更新文件时间
open -e .bash_profile // 打开文件
```

然后在打开的文件中加入下面的内容：

```bash
export PATH=$PATH:/Users/smyhvae/Dev/Android/adt-bundle-mac-x86_64/sdk/platform-tools
```

最后输入如下命令：（使用刚才更新之后的内容）

```bash
source .bash_profile
```

此时，adb环境就配置好了。在终端输入`adb`即可进行检验。


部分命令解释：
open .bash_profile：打开文件
touch .bash_profile：如果没有，则创建文件；如果有，更新一下文件时间.
open -e bash_profile：编辑文件


参考链接：

- [mac下环境变量的配置（以android adb为例）](http://www.jianshu.com/p/618d55a79832)



### ADT相关

**方法一：**ADT Bundle（不推荐）


从官网下载好[ADT Bundle](https://dl.google.com/android/adt/adt-bundle-mac-x86_64-20140702.zip)之后，打开eclipse.app，提示：`您需要安装旧java SE 6 运行环境才能打开Eclipse.app`。在当前画面点击「查看更多」，会自动跳到apple官网链接，下载对应版本的jdk 1.6进行安装即可。

好吧，等我根据提示安装好了之后，再打开eclipse，程序报错。算了，这个方法不行，我估计是MacOS的版本太高了，不支持低版本的jdk。


参考链接：

- [](http://www.cnblogs.com/zhouyinhui/p/3751389.html)


**方法二：**Eclipse for android（不推荐）

Mac下adt-bundle不太好用.其实Eclipse官网本身提供了与Android集成的Eclipse版本，使用了下相当不错，大家可以试试,下载地址：<http://www.eclipse.org/downloads/eclipse-packages/>


然后我去官网下载了最新版的Eclipse for android（eclipse-android-neon-1a-incubation-macosx-cocoa-x86_64），安装完了之后，提示我说jdk版本太低了（我的是jdk 1.7，提示说要安装1.8）。好吧，那我就把jdk版本升级为1.8吧。

终于安装好了，打开Eclipse，也能新建android工程，但是新建完了之后，工程文件报错：failed to load properties file for project、`R cannot be resolved to a variable（即没有生成 R 文件）`。网上查了一下，原因是SDK中需要下载最新的Build Tools。

另外，新建的安卓项目有mipmap目录（我的Eclipse版本 Neon Release (4.6.0)），我们需要把xml中的资源文件的引用从drawable改为mipmap。此时，工程就不再报错了。

参考链接：

- [Mac Android 开发环境 adt-bundle 常见问题](http://www.jianshu.com/p/cebc3f8b8f88)



**方法三：在Eclipse中离线安装ADT插件**（推荐）

相关版本信息：

- MacOS版本：10.12.1
- jdk版本：jdk-8u77-macosx-x64.dmg
- 「Eclipse IDE for java Developers」版本: Mars.2 Release (4.5.2)
- ADT-23.0.2.zip


下载历史版本的celipse 4.5.2。下载链接：<http://archive.eclipse.org/eclipse/downloads/>。然后，离线安装ADT。**离线安装ADT插件的步骤如下：**

（1）启动 Eclipse ；选择「Help > Install New Software」，在右上角点击「add」，然后点击「Archive」进行本地安装；选择下载的文件 adt-23.0.2.zip  并点击 OK 。

（2）然后经过Pending解析后，就可以看到对应的：Developer Tools，选中Developer Tools，并去掉对话框的左下角最下面的一个选项前的对勾，不然会安装的很慢：

20161206_1340.png

（3）然后一路Next，点击接受协议和完成；中间会有安全提示，点击OK即可。安装完毕后，会要求重启Eclipse。大功告成。

第一次重启后，软件会提示你设置Android SDK路径，那就加载之前下载好的SDK即可。如下图所示：

20161206_1347.png

上图中的选项，在「Eclipse- 偏好设置- Android」中也可以设置。


之后，关掉Eclipse，新建一个workspace，然后就可以新建一个新的Android projct了。

这里注意：一定不要升级android sdk tools（23.0.2） 和android sdk platform－tools(20)，因为有可能会出现环境错误。20161207_1955.png



参考链接：

- [Eclipse中离线安装ADT插件](https://github.com/inferjay/AndroidDevTools/wiki/Eclipse%E4%B8%AD%E7%A6%BB%E7%BA%BF%E5%AE%89%E8%A3%85ADT%E6%8F%92%E4%BB%B6)

- ADT的历史版本下载链接：<https://downloads.puresoftware.org/files/android/ADT/>


打开Eclipse，新建一个Android工程，如果报错如下：

```bah
Errors occurred during the build.
Errors running builder 'Android Resource Manager' 
```

我照着网上的教程操作了一下。解决办法如下：（并没有解决我的问题）

（1）找到Eclipse的目录，在Eclipse上右击，选择“显示包内容”；

（2）找到/Contents/Eclipse/eclipse.ini文件，这个就是我们要修改的文件

（3）找到“-vmargs”，在其前面添加如下内容：

```bash
-vm  
/System/Library/Frameworks/JavaVM.framework/Versions/1.6/Commands/java
```

一部分原因是不应该升级sdk tools的版本；另一部分原因是要保证jdk版本是1.8（1.7的也会报这个错）

参考链接：

- [Errors running builder 'Android Resource Manager' on Project java.lang.NullPointerException](http://blog.csdn.net/gtsong/article/details/39481879)

-  [在MAC上搭建eclipse+android开发环境(荐)](http://jingyan.baidu.com/article/455a9950b66eb2a1662778ee.html)


### Android Studio


### SourceTree

Git版本控制的GUI工具。官网链接：<https://www.sourcetreeapp.com>。类似的软件还有[TortoiseGit](https://tortoisegit.org/)。



### vmware



安装包下载链接：<http://xclient.info/s/vmware-fusion.html>




[1]:	https://itunes.apple.com/cn/app/jie-tu-jietu/id1059334054?mt=12
[3]:	http://nssurge.com/
[4]:	
[5]:	https://www.google.com/chrome/browser/thankyou.html?standalone=1&platform=mac&installdataindex=defaultbrowser#
[6]:	https://ii-i.org/archives/8
