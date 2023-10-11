


> 积累千古壹号平时遇到的 MacTips。第一次使用 Mac 时，很有用。

### 无法打开 xxx 软件，因为Apple无法检查其是否包含恶意软件

解决办法：打开设置中的“隐私与安全性-->安全性设置”，点击“仍要打开”按钮，即可打开被阻止的 App。此按钮在你尝试打开该 App 后一小时内可用。


参考链接：[Apple 无法检查 App 是否包含恶意软件](https://support.apple.com/zh-cn/guide/mac-help/mchleab3a043/mac)


### Mac M1 芯片的电脑，安装 Git

不需要安装 Xcode，这个太大了，好几个G。直接安装 [Command Line Tools for Xcode](https://developer.apple.com/download/all/?q=command) 即可，安装完成后 Git 就有了。

参考链接：

- [macos m1 安装git，终端运行git命令提示安装 Xcode](https://blog.csdn.net/A_Brave/article/details/120844682)


### git clone 时，提示错误：Failed to connect to github.com port 443: Connection refused

解决办法：

```bash
# 这行命令可以不需要
git config --global http.sslVerify "false"
image.png
# 重点是下面这两行命令，把端口号 7890 换成你自己的代理软件的端口号
git config --global https.proxy http://127.0.0.1:7890
git config --global http.proxy http://127.0.0.1:7890
```

参考链接：

- [Failed to connect to github.com port 443: Operation timed out - 烟霞志](https://simplestark.com/archives/%E7%BB%8F%E9%AA%8C%E5%AE%9D%E5%AE%9Dfailedtoconnecttogithubcomport443operationtimedout)


- [解决 Failed to connect to github.com port 443:connection timed out_fK0pS的博客-CSDN博客](https://blog.csdn.net/Hodors/article/details/103226958)



### Alfred的自动粘贴功能 Auto-Paste on return 失效，如何解决

解决办法：

1、打开 Alfred Preferences 偏好设置，找到 Features — Clipboard History — Advanced，确保开启了Auto-Paste on return（回车时自动粘贴）功能。

2、打开系统偏好设置 — 安全性与隐私 — 隐私 - 辅助功能，将 Alfred 勾选上。


### 外接键盘的键位，映射修改

将 cmd 改为 option，将 option 改为 cmd。

![](https://img.smyhvae.com/20220615_1905.png)

### Mac到底要不要关机

对于关机，我的观点是：

- 如果每天用，建议 Mac 不关机，使用睡眠模式；
- 如果不常用，建议 Mac 关机。

具体可以看这篇文章：[Mac 到底要不要关机？| 领客专栏 · MacTips](http://www.ifanr.com/app/657745)




### 重置 SMC

如果发现 Macbook Pro 的某一个 Type-C 失效了，能充电，但是 HDMI 和 USB 网络都不行，此时可以重置 SMC。

重置  SMC 是个 Mac 常用操作，电源、背光、亮屏、不能充电等等，都可以以此解决，不过很多人不知道。如何 重置 SMC 呢？

1、将 Mac 关机。
2、在内建键盘上，按下键盘左侧的 Shift-Control-Option 键，然后同时按下电源按钮。按住这些按键和电源按钮 10 秒钟。
如果您的 MacBook Pro 带有 Touch ID，则 Touch ID 按钮也是电源按钮。
3、松开所有按键。
4、再次按下电源按钮以开启 Mac。



### 卸载软件后，清除残留

虽然程序已经被删除了，但硬盘上可能会有残留文件。这些文件占内存小，如果你之后重新安装该应用程序的话，它们是会保留的。但如果以后再也不用的话，可以选择彻底删除。


步骤如下：

（1）打开资源库Library：按住⌥ Option键，单击“前往”菜单，菜单下就会出现“资源库”选项。
（2）删除缓存：在`Application Support`（应用程序支持）目录里，删除对应软件的文件夹。
（3）删除偏好设置：在`Preferences`（偏好设置）目录里，删掉对应软件的偏好设置文件。


温馨提示：

在终端输入命令`chflags nohidden ~/Library`，可以永久显示资源库Library文件夹。

参考链接：

- [wikiHow](https://zh.wikihow.com/%E5%9C%A8Mac%E4%B8%8A%E5%8D%B8%E8%BD%BD%E7%A8%8B%E5%BA%8F)



### Mac 备份微信聊天记录的问题（20180218）

问题描述：MAC版微信可以备份手机聊天记录到电脑了，但是手机和电脑明明是在同一个网络了，却说不在。手机显示的是网络名称，电脑的网络显示的是***的macbook。

解决：把电脑里“设置-共享”里面的名称改为Wi-Fi的名称，就可以备份。

PS：网上都是这个答案，但是我自己试了一下，还是不行。


### 电脑锁屏（20180220）

问题描述：把电脑合上以后（或者按 Touch Bar上的锁定键后），再立即打开电脑，发现电脑并没有锁屏。原因是需要设置锁屏的时间。

解决：「系统偏好设置 -->安全与隐私 --> 通用 --> 进入睡眠或开始屏幕保护程序 --> 选择“立即”」。


### 修改host文件


点击 Finder，在顶部菜单栏选择“前往”－“前往文件夹”，粘入 `/private/etc/` 这个路径（不带引号），找到`hosts`文件。


### iPad上取消爱奇艺会员的续费

![](http://img.smyhvae.com/20180426_2338.png)


### Android手机连接Mac


### mac下的局域网共享

参考链接：<https://zhidao.baidu.com/question/368299591.html>


### Mac日历设置生日提醒

1、iCloud 开启同步日历。

2、通讯录里设置农历生日。

3、日历里设置提醒时间（默认是提前一天）。

20180725_1918.png


### Mac版微信备份时，提示“请将手机和电脑连接至同一网络后”

问题描述：我的Mac和手机，已经在同一网络下了，但在备份聊天记录时，依然提示“请将手机和电脑连接至同一网络后”。

解决办法：

把电脑里**“设置-共享”**里面的名称改为Wi-Fi的名称，就可以备份了。

### 放大/缩小 Mac 微信的分辨率

快捷键：Cmd + +/-


### 014 管理 iCloud 储存空间

- 在 iPhone、iPad 或 iPod touch 上：如果您使用的是 iOS 10.3 或更高版本，请前往“设置”>“[您的姓名]”>“iCloud”。轻点“iCloud 储存空间”或“管理储存空间”。

- 在 Mac 上，前往苹果菜单 「 --> 系统偏好设置 --> Apple ID（互联网账户）--> iCloud」，然后点击「管理」。

- 在 PC 上，请打开 Windows 版 iCloud。

- 在支持的浏览器上，登录 iCloud.com。



参考链接：<https://support.apple.com/zh-cn/HT204247>


### Mac 版印象笔记，美化 Markdown 样式

参考链接：

- <https://github.com/timothyzhw/evernote-markdown-vue>

- <https://www.jianshu.com/p/1e7e0a975d30>

操作步骤：

（1）下载主题中的vue.css文件，以及包含字体的vue文件夹，拷贝到 目录`/Applications/印象笔记.app/Contents/Resources/common-markdown-mac/`下。

（2）打开目录`/Applications/印象笔记.app/Contents/Resources/common-markdown-mac/`，编辑里面的 `index.html`文件，在最后一行`</html>`前插入如下代码：

```
  <link href="vue.css" rel="stylesheet">

```

（3）重启印象笔记。



美化效果：

![](http://img.smyhvae.com/20191210_1615.png)


**【补充】个性化配置**



（1）我们还可以增大段落之间的行距。在 vue.css 文件中，找到如下代码：

```css
.tui-editor-contents p {
    line-height: 1.6rem;
    word-spacing: .05rem;
}

```

将上方代码修改为：

```css
.tui-editor-contents p {
    line-height: 1.6rem;
    word-spacing: .05rem;
    margin-bottom: 1.2rem;
}
```

其实就是加了一行 `margin-bottom: 1.2rem;` 就搞定了。


（2）修改二级标题的字体大小和颜色：

找到如下代码：

```css
.tui-editor-contents h2 {
    font-size: 24px;
    border-bottom: 1px solid #ddd;
    color: #2c3e50
}
```

修改为：

```css
.tui-editor-contents h2 {
    font-size: 1.5rem;
    border-bottom: 1px solid #ddd;
    color: #24292e
}
```

另外，我们还可以修改三级标题的 font-size 为 1.25rem。


### 让 Dock 只显示已打开的应用程序

> 这个功能，我都用的少，因为不习惯。

**背景**：

默认情况下，Dock 栏不仅会显示已打开的应用程序，还会显示最近打开过的应用程序（无论打开与否）。

这种「一个不漏」的显示方式，并不是太好：

- 对那些已经有不少在 Dock 中保留的项目的用户来说，随着新增的应用图标和最小化窗口的挤占，Dock 栏会越变越小。这时，Dock 中不活跃的应用程序会影响操作效率。

- 对那些希望截取或录制屏幕内容的用户来说，为了保持内容的相关性，常常会在截取或录制之前将不需要的项目从 Dock 栏中移除，结束后再加以恢复，十分费力。

**操作如下**：

![](http://img.smyhvae.com/20200313_1935.png)

参考链接：[装点你的 Dock：外观篇丨一日一技 · Mac](https://sspai.com/post/33493)



### 如何解决MAC软件（dmg，akp，app）出现程序已损坏的提示

「xxx.app已损坏,打不开.你应该将它移到废纸篓」，并非你安装的软件已损坏，而是Mac系统的安全设置问题，因为这些应用都是破解或者汉化的,那么解决方法就是临时改变Mac系统安全设置。

出现这个问题的解决方法：修改系统配置：系统偏好设置... -> 安全性与隐私。修改为任何来源。

如果没有这个选项的话（macOS Sierra 10.12）,打开终端，执行：

```bash
sudo spctl --master-disable
```

即可。


### Mac “永久” 隐藏Dock

> 比较实用

正常情况下，将 Dock 隐藏之后，鼠标悬停在屏幕底部时，Dock 还是会出现。那要如何“永久”隐藏 Dock呢？答案是：更改 Dock 出现的时间就好了。操作如下。

**设置dockc出现的时间**：（在终端输入如下命令）

```bash
#先修改停留时间（后面数字为停留时间）如：
defaults write com.apple.dock autohide-delay -int 0      ##（时间设为最短）
defaults write com.apple.dock autohide-delay -int 0.5    ##（时间设为 0.5s）
defaults write com.apple.dock autohide-delay -int 10     ##（时间设为 10s）

#使设置生效
killall Dock
```

参考链接：[Mac “永久” 隐藏Dock](https://www.jianshu.com/p/47cbd4f5e4c3)


### 使用命令行来批量添加文件扩展名

参考链接：

- [Mac下如何使用命令行来批量添加文件扩展名](http://www.sdifen.com/mac-rename.html)

### Mac 修改终端用户名

```
sudo scutil --set HostName xx
```

然后关掉当前终端，重新开一个终端就好了。