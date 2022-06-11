---
title: Sublime Text快捷键
date: 2016-05-18 12:39:04
categories:
- 技术
tags:
- 工具
---



## 下载

- [Sublime Text 3 官方下载地址](http://www.sublimetext.com/3)

## 注册码


### Sublime Text 3 3126

- [Sublime Text 3 3126 注册码](https://fatesinger.com/78705)


### Sublime Text 3 3143

注册码：

```
—– BEGIN LICENSE —–
TwitterInc
200 User License
EA7E-890007
1D77F72E 390CDD93 4DCBA022 FAF60790
61AA12C0 A37081C5 D0316412 4584D136
94D7F7D4 95BC8C1C 527DA828 560BB037
D1EDDD8C AE7B379F 50C9D69D B35179EF
2FE898C4 8E4277A8 555CE714 E1FB0E43
D5D52613 C3D12E98 BC49967F 7652EED2
9D2D2E61 67610860 6D338B72 5CF95C69
E36B85CC 84991F19 7575D828 470A92AB
—— END LICENSE ——
```

参考链接：

- [csdn](http://blog.csdn.net/weixin_39768635/article/details/77979793)






## 个人最常用的快捷键

快捷键完整版见最后一段，本段只列个人习惯。

**四种 Goto ：**

- `Ctrl + P`：文件定位

- `Ctrl + ;`：词语定位 #

- `Ctrl + R`：函数定位 @

- `Ctrl + G`：行号定位 :



## 编辑器配置

**修改配置路径：**Sublime Text -> Preferences -> Settings-User

以下配置，可以根据个人喜好可以进行修改。



```bash

"always_show_minimap_viewport": true, #是否总是显示小地图
"draw_minimap_border": true, # 让minimap里的当前位置更显眼点.
"highlight_modified_tabs": true, # 修改了而尚未保存的 tab, 会用橘黄色显示
"ignored_packages":
[
   "Vintage"
],
"show_full_path": true, # 标题栏上显示完整路径
"show_line_endings": true, # 文档到达底部会在最后一行
"open_files_in_new_window": false, #  在 Finder 里打开文件时, 不会新开窗口了
"translate_tabs_to_spaces": true #将tab键的形式转成空格
```


#### 高亮当前行

```bash
"highlight_line": true
```

这个设置会让让光标所处在的那一行高亮，只是稍微亮一点，但你可以立马找到他。

### 焦点丢失后自动保存

```bash
"save_on_focus_lost": true
```

顾名思义，当你把焦点从当前编辑的文件移开的时候，这个文件会自动的保存掉。估计很多人有时会呆呆的调试一个没有保存的文件，所以这个设置可以说是一个必需品。


### 保存的时候把无用的空格去掉

```bash
"trim_trailing_white_space_on_save": true
```

这里去掉的是每一行文本最后面的空格，这些空格显然是没有什么用处的。如果手动去删除和检查的话，估计你会很烦心。当然至于要不要删掉，还是看你的需求。


#### 显示当前文件的编码

```
"show_encoding": true
```

为了避免一些低级错误，这个设置还是相当有用的。当你开启后，在编辑器的右下角会显示当前文件的编码。


#### 在新标签页中打开新的文件


```bash
"preview_on_click": false
```

默认的配置项中，单击一个新的文件后，会覆盖当前的标签页，这种体验很不好。`"open_files_in_new_window": true`这个设置项默认已经有了，但并没有达到预期的效果。

如果想在新的标签页中打开新的文件，可以设置此参数；设置后，打开文件需要双击。


还有一种方法是尝试增加属性`"preview_on_click": false`，但是这样的话，需要双击才能打开新的文件。体验不好。


使用新标签打开文件，防止把以前打开的文件给覆盖掉。


参考链接：

- [segmentfault](https://segmentfault.com/a/1190000002596724)

- [MAC全栈开发环境搭建指南](https://mac.aotu.io/docs/dev-fd/sublime-text.html)


## 插件


### 安装Package Control

**方法一：**

先装插件管理器：[Package Control](https://packagecontrol.io/installation)，用它我们可以很方便的浏览、安装和卸载Sublime Text中的插件。步骤如下：

（1）使用「Ctrl + `」打开Sublime Text控制台，将下面的代码粘贴到控制台里：

```
import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())
```


等待Package Control安装完成。

重启。

如果顺利的话，此时就可以在Preferences菜单下看到Package Settings和Package Control两个菜单了。


（2）用`Ctrl + Shift + P`打开命令板，输入`PCI`应出现Package Control。此时表明安装成功。

之后，我们就可以方便的安装使用Sublime Text的各种插件了。


**方法二：**（Sublime Text 3143的安装）


如果安装的是Sublime Text 3143，上面的方法一可能会失效。此时可尝试方法二。

方法二在我的mac上可行，在我的win上不可行。


**方法二：**（离线安装）


方法二应该对所有版本的Sublime Text均适用。步骤如下。

- 关闭Sublime Text 3，去<https://github.com/wbond/package_control/releases>下载一个zip包。
- 将包内的顶层文件夹解压至C:\Users\<你的用户名>\AppData\Roaming\Sublime Text 3\Packages路径下（找不到AppData的请显示系统文件夹及隐藏文件夹，或者直接在地址中输入该路径），重命名package_control-3.3.1-beta2（与下载版本名称有关）为Package Control
- 打开Sublime Text 3（刚打开时会自动安装Package Control，按`Ctrl+`可以在控制台中查看进度），安装完Package Control后按Ctrl+Shift+P，输入“Install”来搜索Package Control。


参考链接：[csdn](http://blog.csdn.net/swhard/article/details/78930371)


### 无法安装插件的问题

Package control 好不容易安装好了，当你尝试去安装别的插件的时候，可能发现报错如下：

```
 There are no packages available for installation
```

解决办法如下：


打开目录`C:\Users\smyhvae\AppData\Roaming\Sublime Text 3\Packages\User\`下的`Package Control.sublime-settings`文件，添加一行"channels"字段：

```bash

"channels":
[
	"https://wilon.github.io/static/channel_v3.json"
],
```

上面的"channels"字段是添加的url路径。如果认为上面的链接太慢，还可以指定本地的channel_v3.json路径（推荐此方法），方法如下：

- 下载json文件：packagecontrol.io下载 或 [GitHub下载](https://wilon.github.io/static/channel_v3.json)
- 将下载好的文件放到Sublime Text的安装目录下。
- 将上面的"channels"字段改为

```bash
"channels":
[
	"C:/Program Files/Sublime Text 3/channel_v3.json"
],
```


参考链接：

- [知乎](https://www.zhihu.com/question/34386189/answer/80188612)

- [csdn](http://blog.csdn.net/q2365921/article/details/74298371)



### 中文输入法中，光标无法跟随

解决办法：安装`IMESupport`这个插件。貌似目前只支持windows，在搜索等界面不能很好的跟随光标。

操作：Ctrl + Shift + P →输入pci →输入IMESupport →回车。


### 中文乱码的问题

解决办法：安装插件`ConvertToUTF8`。

如果是在Mac上使用的话，还得安装一个插件`Codecs33`



### 在Sublime Text中进行markdown写作

**（1）安装主题：实现markdown语法高亮。**

安装  Package Control之后，安装插件`Monokai Extended`和`Markdown Extended`。步骤如下：

- Shift + Command + P 调出 Command Palette，输入 pci（模糊匹配），找到 Package Control: Install Package，回车;
- 分别输入两个插件名称、回车，等待安装；
- 点击 Sublime 右下角文档格式，在列表最上方名为 Open all with current extension as 二级列表中选择 Markdown Extended；
- 在 Preferences——Color Scheme——Mononkai Extended 下选择一个皮肤，我选的是`Bright主题`。效果如下：

参考链接：[确实是近乎完美的 markdown 写作体验](https://wzzlj.gitbooks.io/wzzljomooc2py/content/Begin/peizhi_sublime_markdown.html)

上面这个链接也讲到了gitbook的使用，可以参考下。

，再推荐一个很漂亮的主题：[Material Theme](https://github.com/equinusocio/material-theme)

**（2）实现实时预览：**

同样是在`install package`中安装插件`OmniMarkupPreviewer`。因为网的原因，这个插件安装的时间会比较久。

插件安装成功后我们就可以使用快捷键对编辑的markdown源文件进行预览了。下面是几个常用快捷键：

- **Ctrl + Alt + O**：在浏览器中**实时预览**（非常实用）
- Ctrl + Alt + X：导出HTML
- Ctrl+Alt+C：HTML标记拷贝至剪贴板

参考链接：[介绍Sublime3下两款Markdown插件](http://www.jianshu.com/p/335b7d1be39e)

预览的时候，如果出现下面这样的错误：

![](http://img.smyhvae.com/201801101430.png)

解决办法：

Sublime Text > Preferences > Package Settings > OmniMarkupPreviewer > Settings - User。复制粘贴下面代码保存：

```bash
{
    "renderer_options-MarkdownRenderer": {
        "extensions": ["tables", "fenced_code", "codehilite"]
    }
}
```

参考链接：

- [关于OmniMarkupPreviewer 404](https://www.jianshu.com/p/d8367fec0edf)
- [issues](https://github.com/timonwong/OmniMarkupPreviewer/issues/85)


### 侧边栏增强插件：SideBarEnhancements

侧边栏右键的时候，默认选项比较少；

20180110_2023.png

安装了插件`SideBarEnhancements`之后，侧边栏的选项变多了：

20180110_2029.png


### 其他插件

- `Bracket Highlighter`：匹配括号高亮，自带的感觉高亮不强。

- `Emmet`：前端工程师利器，各种代码补全自动生成。





## 使用技巧

### 在Sublime Text 中进行代码格式化

其实在sublime中已经自建了格式化按钮：

Edit  ->  Line  ->  Reindent  ｝

只是sublime并没有给他赋予快捷键，所以只需加上快捷键即可。



参考链接：[Sublime 格式化代码 快捷键以及插件使用](http://blog.csdn.net/vic___/article/details/12615089)


### 鼠标中键的使用

按住鼠标中键，往下拖动（不是滚动鼠标），它达到的效果等同于：Ctrl+鼠标左键单击。



## mac下的使用

### 字体放大缩小

快捷键：`command + 加号`是放大字体。



## 快捷键汇总


### 编辑

| Win快捷键 |Mac快捷键| 作用 | 备注 |
|:-------------|:-------------|:-----|:-----|
| Ctrl + Enter || 在当前行下面新增一行然后跳至该行 | 即使光标不在行尾，也能快速向下插入一行。 |
| Ctrl + Shift + Enter | |在当前行上面增加一行并跳至该行  |   |
|  **Ctrl + Shift + D** | |复制当前行到下一行  |   |
|  **Ctrl+K+K** ||  从光标处开始删除代码至行尾。按住Ctrl，按两次K |   |
|  Ctrl+Shift+K ||  删除整行 |   |
|Ctrl+H|Option+Cmd+F|查找替换|||
| Ctrl+/  ||  注释单行 |   |
| Ctrl+Shift+/  || 注释多行  |   |
|  Ctrl+K+U ||  转换大写 |   |
| Ctrl+K+L  ||  转换小写 |   |
|  Ctrl+F2 ||  设置书签，F2切换书签* |   |
|  Ctrl+T ||  左右字母互换 |   |
| F6  || 单词检测拼写 |   |
|   |   |   ||



### 选择

| Win快捷键 | Mac快捷键 | 作用 | 备注 |
|:-------------|:-------------|:-----|:-----|
|Ctrl+鼠标左键单击||集体输入||
|Ctrl + D||选择当前光标所在的词并高亮该词所有出现的位置，再次按`Ctrl + D`选择该词出现的下一个位置。|在多重选词的过程中，使用`Ctrl + K`进行跳过，使用`Ctrl + U`进行回退，使用`Esc`退出多重编辑|
|**Alt + F3**| | 选中文本按下快捷键，即可一次性选择全部的相同文本进行同时编辑| 例如快速选中并更改所有相同的变量名、函数名等。|
|**Ctrl + Shift +【↑/↓**| Ctrl + Cmd +↑/↓ | 移动当前行 | |
|Ctrl+L| | 选中整行，继续操作则继续选择下一行，效果和 `Shift + ↓` 效果一样| |
|**Ctrl+Shift+L**| | 先选中多行，再按下快捷键，会在每行行尾插入光标，即可同时编辑这些行| 经常与上一个快捷键结合起来使用 |
|**Ctrl + J**| | 把当前选中区域合并为一行| |
| Ctrl + ←/→| | 进行逐词移动| |
|Ctrl + ↑/↓| | 移动当前显示区域| |
|Shift + ↑/↓|| 一行一行地进行选中| |
|Ctrl + Shift + ←/→| | 进行逐词选择| |
|Ctrl + M| |光标移动至括号内结束或开始的位置||
|Ctrl + Shift + M| |快速选择括号间的内容| |
|Ctrl + Shift + J| |快速选择同缩进的内容| |
|Ctrl + Shift + Space| |快速选择当前作用域（Scope）的内容| |
|Ctrl+Shift+[| |选中代码，按下快捷键，折叠代码。| |
|Ctrl+Shift+]| |选中代码，按下快捷键，展开代码。| |
|Ctrl+K+0| |展开所有折叠代码。| |

### 多重选择（Multi-Selection）

多重选择功能允许在页面中同时存在多个光标，让很多本来需要正则表达式、高级搜索和替换才能完成的任务也变得游刃有余。

激活多重选择的方法有两几种：

- 按住 Ctrl 然后在页面中希望中现光标的位置点击。
- 选择数行文本，然后按下 Shift + Ctrl + L。
通过反复按下 Ctrl + D 即可将全文中与光标当前所在位置的词相同的词逐一加入选择，而直接按下 Alt+F3即可一次性选择所有相同的词。
- 按下鼠标中键来进行垂直方向的纵列选择，也可以进入多重编辑状态。



### 搜索

- `Ctrl + Shift + F`：多文件查找&替换

在文件夹内查找，与普通编辑器不同的地方是sublime允许添加多个文件夹进行查找。



- `F3`：跳至当前关键字下一个位置

- `Shift + F3`：跳到当前关键字上一个位置


- `Ctrl + F/H`：进行标准查找/替换，之后：

- `Alt + C`：切换大小写敏感（Case-sensitive）模式

- `Alt + W`：切换整字匹配（Whole matching）模式

- `Alt + R`：切换正则匹配（Regex matching）模式

- `Ctrl + Shift + H`：替换当前关键字

- `Ctrl + Alt + Enter`：替换所有关键字匹配



- `Ctrl + P：打开搜索框，跳转到指定文件。输入文件名后可以：

- 输入当前项目中的文件名，快速搜索文件；

- 输入@和关键字，查找文件中函数名；

- 输入：和数字，跳转到文件中该行代码；

- 输入#和关键字，查找变量名

- `Ctrl + R`：打开搜索框，自带`@`，输入关键字，查找文件中的函数名。

例如：在函数较多的页面快速查找某个函数。

- `Ctrl + G`：打开搜索框，自动带`:`，输入数字跳转到该行代码。

例如：在页面代码比较长的文件中快速定位。

- `Ctrl+ `：打开搜索框，自动带`@`，输入关键字，查找文件中的函数名。

例如：在函数较多的页面快速查找某个函数。



### 显示

| 快捷键 | 作用 | 备注 |
|:-------------|:-------------|:-----|
|  Ctrl+Tab | 按文件浏览过的顺序，切换当前窗口的标签页 |   |
|  Ctrl+PageDown |  向左切换当前窗口的标签页 |   |
|  Ctrl+PageUp |  向右切换当前窗口的标签页 |   |
|  F11 |  普通全屏 |   |
|  Shift + F11 | 免打扰全屏  |   |
|  Alt + Shift + 1 |  窗口分屏，恢复默认1屏 |  非小键盘的数字 |
|  Alt + Shift + 2 |  左右分屏-2列 |   |
| Alt + Shift + 3  |  左右分屏-3列 |   |
| Alt + Shift + 4  |  左右分屏-4列 |   |
|  Alt + Shift + 5 |  上下左右分屏-等分4屏 |   |
|  Alt + Shift + 8 | 上下分屏-2行  |   |
|  Alt + Shift + 9 | 上下分屏-3行  |   |
|  Ctrl+K+B | 开启/关闭侧边栏  |   |
|   |   |   |

备注：分屏之后，使用`Ctrl + 数字键`跳转到指定屏，使用`Ctrl + Shift + 数字键`将当前屏移动到指定屏




### 窗口

`Ctrl + N`：在当前窗口创建一个新标签

`Ctrl + Shift + N`：创建一个新窗口

`Ctrl + Shift + T`：恢复刚刚关闭的标签

### 其他

- `Ctrl + Shift + P`：调出命令板（Command Palette）

- `Ctrl + `：调出控制台


## 参考链接

- [Sublime Text 全程指引 by Lucida](http://www.cnblogs.com/figure9/p/sublime-text-complete-guide.html)【荐】

- [我的Sublime Text 3 配置](http://lovenight.github.io/2015/11/30/%E6%88%91%E7%9A%84Sublime-Text-3-%E9%85%8D%E7%BD%AE/)

- [知乎：Sublime Text 有哪些实用技巧？](https://www.zhihu.com/question/19976788)

- [如何优雅地使用Sublime Text3](http://www.jeffjade.com/2015/12/15/2015-04-17-toss-sublime-text/)

- [面向 Web 开发者的 Sublime Text 插件](http://chinagdg.org/2016/02/ttt1-sublime-plugins/)

- [Sublime Text 3最好的功能、插件和设置](http://www.css88.com/archives/5858)

- [Sublime Text：我的极简 Markdown 编辑器](http://tinyletter.com/CnFeat/letters/sublime-text-markdown)

- [如何优雅地使用 Sublime Text3 [OS X]](http://qiudeqing.com/tools/2015/05/31/sublime-text-3.html)

- [Seti UI 主题: 让你编辑器焕然一新](http://chinagdg.org/2016/02/ttt2-seti-ui/)

- [Sublime Text 3 配置和使用方法](https://www.zybuluo.com/king/note/47271)


- [20 个强大的 Sublime Text 插件](http://www.oschina.net/translate/20-powerful-sublimetext-plugins)

- [像 Sublime Text 一样使用 Chrome DevTools](http://chinagdg.org/2015/12/%E5%83%8F-sublime-text-%E4%B8%80%E6%A0%B7%E4%BD%BF%E7%94%A8-chrome-devtools/)

网站的这篇文章也可以看看：[http://chinagdg.org/2016/04/android-studio-2-0/](http://chinagdg.org/2016/04/android-studio-2-0/)


- [sublime text插件推荐](http://w3cboy.com/post/2014/01/sublime%E6%8F%92%E4%BB%B6%E6%8E%A8%E8%8D%90/)


- [ Sublime Text3 快捷键汇总及设置快捷键配置环境变量](http://blog.csdn.net/moyan_min/article/details/11530751)

传智播客推荐的参考链接。

### mac篇

- [Sublime Text 3 Mac 指南](https://code.kpman.cc/2014/10/14/sublime-text-3-mac-%E6%8C%87%E5%8D%97/)


### 2018-06-24

- [将 Sublime Text 打造成微信公众号文章编辑排版神器（一）](https://mp.weixin.qq.com/s/N2O7MZi3InGTKeBhY2Ut2g)


- [将 Sublime Text 打造成微信公众号文章编辑排版神器（二）](https://mp.weixin.qq.com/s/QnrIz40XD3_8jCQ_ykWDqg)

- [将 Sublime Text 打造成微信公众号文章编辑排版神器（三）](https://mp.weixin.qq.com/s/bBwR8rKrrdeWu1ckP_LdSg)


### markdown 相关


- [Sublime Text3 Markdown 编辑 + 实时预览](https://juejin.im/post/5c1609b2e51d45766d4e9bad)







