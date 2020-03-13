

### 让 Dock 只显示已打开的应用程序

**背景**：

默认情况下，Dock 栏不仅会显示已打开的应用程序，还会显示最近打开过的应用程序（无论打开与否）。

这种「一个不漏」的显示方式，并不是太好：

- 对那些已经有不少在 Dock 中保留的项目的用户来说，随着新增的应用图标和最小化窗口的挤占，Dock 栏会越变越小。这时，Dock 中不活跃的应用程序会影响操作效率。

- 对那些希望截取或录制屏幕内容的用户来说，为了保持内容的相关性，常常会在截取或录制之前将不需要的项目从 Dock 栏中移除，结束后再加以恢复，十分费力。

**操作如下**：

![](http://img.smyhvae.com/20200313_1935.png)

参考链接：[装点你的 Dock：外观篇丨一日一技 · Mac](https://sspai.com/post/33493)


### Mac “永久” 隐藏Dock

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





























