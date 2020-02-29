

## 前言


对于经常阅读的人来说，制作本地电子书，算是刚需了。

网上的很多步骤不太完整，所以我特地整理出一个详细的教程。亲测有效，一劳永逸。

大致的思路是：

- 本地安装 gitbook

- 安装 calibre，配置ebook-convert

- 导出epub电子书（或者mobi、pdf），完善目录结构

## 使用步骤

### 步骤1：通过 npm 安装 gitbook-cli

安装命令如下：

```
npm install -g gitbook-cli
```

PS：如果你不知道 `npm` 是什么，可以自行查阅**如何安装 npm 环境**。

### 步骤2：安装ebook-convert

（1）Mac 系统需要先安装 [calibre](https://calibre-ebook.com/download) 软件。安装完成后，执行如下命令：

```
sudo ln -s /Applications/calibre.app/Contents/MacOS/ebook-convert /usr/bin
```

如果出现`Operation not permitted`异常，说明系统权限限制，此时需要**配置环境变量**。

（2）环境变量配置：

```bash
vim ~/.bash_profile

export EBOOK_PATH=/Applications/calibre.app/Contents/MacOS
export PATH=$PATH:$EBOOK_PATH
```

然后刷新一下刚刚的配置：

```
source ~/.bash_profile
```

验证`ebook-convert`指令是否能正常被调用：

```
ebook-convert --version
```


### 步骤3：导出电子书

本地新建一个空的文件夹，作为项目。

（1）在当前项目下，执行如下命令，进行初始化：

```
gitbook init
```

此时，项目下会自动生成如下两个文件：（**非常重要**）

- `README.md`：书籍的介绍写在这个文件里。

- `SUMMARY.md`：书籍的**目录结构**在这里配置。


（2）本地预览电子书：

```
gitbook serve
```

执行上方命令后，会对项目里的 Markdown 格式的文件进行转换，默认转换为 html 格式，最后提示 `Serving book on http://localhost:4000`。

我们打开浏览器输入`http://localhost:4000`，预览一下电子书的效果吧。

（3）生成 epub 格式的电子书：（epub是最常见、最通用的电子书格式）

```bash
gitbook epub ./ ./mybook.epub
```

生成 mobi 格式的电子书：

```
gitbook mobi ./ ./mybook.mobi
```

你还可以生成 PDF 格式的电子书：

```
gitbook pdf ./ ./mybook.pdf
```

### 步骤4：配置电子书的目录

我们先把本地的 markdown 文件（也就是我们的**电子书素材**）放到项目中，然后在`SUMMARY.md`文件中配置电子书的目录。举例如下：

```
# 目录

* [前言](README.md)

* [主题介绍](Chapter1/README.md)

* [如何购买](Chapter2/README.md)

* [售后服务](Chapter3/README.md)

* [常见问题](Chapter4/README.md)

* [更新记录](Chapter5/README.md)

	* [# 2018-12-02](Chapter5/20181202.md)
	* [# 2018-12-04](Chapter5/20181204.md)
	* [# 2018-12-05](Chapter5/20181205.md)
	* [# 2018-12-06](Chapter5/20181206.md)
	* [# 2018-12-07](Chapter5/20181207.md)
	* [# 2018-12-10](Chapter5/20181210.md)
	* [# 2018-12-11](Chapter5/2018121.md)
	* [# 2018-12-12](Chapter5/20181212.md)
	* [# 2018-12-13](Chapter5/20181213.md)
  ------
```

制作成的目录效果如下：

![](http://img.smyhvae.com/20190420_1517.png)

### 配置封面

所有格式的电子书都可以配置自定义封面,在项目的根目录下提供 `cover.jpg` 和 `cover_small.jpg` 两种封面图片时，生成电子书会自动增加封面页.

### 参考链接

- 【荐】GitBook使用入门篇，让你快速生成文档(含`SUMMARY.md`目录举例）：<http://www.hehaibao.com/learn-gitbook/>

- 【荐】ebook-convert配置环境变量：<http://gitbook.wiliam.me/ebookandpdf.html>

- gitbook 入门教程之导出电子书：<https://juejin.im/post/5caa0fb46fb9a05e5a2e53b3>

- gitbook 的介绍和使用：<https://snowdreams1006.github.io/myGitbook/experience/gitbook-com.html>


## 进阶篇

### 修改电子书的字体大小

我们还可以在项目的目录下，新建文件`book.json`，用于修改字体大小。








