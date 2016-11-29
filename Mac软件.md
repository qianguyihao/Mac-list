
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


- []()


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

从官网下载好ADT Bundle之后，打开eclipse.app，提示：`您需要安装旧java SE 6 运行环境才能打开Eclipse.app`。

解决办法：打开/Library/Java/JavaVirtualMachines/jdkXXXXX.jdk/Contents/Info.plist 按照如下配置JVMCapabilities中的部分，然后重启计算机。

更改前：

```xml
                <key>JVMCapabilities</key>
                <array>
                        <string>CommandLine</string>
                </array>
```


更改后：

```xml
                <key>JVMCapabilities</key>  
                <array>  
                        　　<string>JNI</string>  
                        　　<string>BundledApp</string>  
                        　　<string>WebStart</string>  
                        　　<string>Applets</string>  
                        　　<string>CommandLine</string>  
                </array> 
```

重启计算机后，重新打开eclipse.app，提示：“打不开Eclipse.app，因为它来自身分不明的开发者。”解决办法：按住control键的同时打开eclipse.app即可。



参考链接：

- [](http://www.cnblogs.com/zhouyinhui/p/3751389.html)




### SourceTree

Git版本控制的GUI工具。官网链接：<https://www.sourcetreeapp.com>。类似的软件还有[TortoiseGit](https://tortoisegit.org/)。







[1]:	https://itunes.apple.com/cn/app/jie-tu-jietu/id1059334054?mt=12
[3]:	http://nssurge.com/
[4]:	
[5]:	https://www.google.com/chrome/browser/thankyou.html?standalone=1&platform=mac&installdataindex=defaultbrowser#
[6]:	https://ii-i.org/archives/8
