
### Node.js 环境安装



### 安装 Python3

1、[官网](https://www.python.org/downloads/macos/)下载安装包，安装 Python。

[安装Python - 廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/1016959663602400/1016959856222624)

2、执行如下命令，安装 pip：

```bash
# 下载脚本
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
# 运行安装脚本
sudo python3 get-pip.py
```

3、执行如下命令，安装 Powerline：

```bash
pip3 install powerline-status

# Find the location
pip3 show powerline-status
```

上方的第一个命令，如果提示`curl: (35) LibreSSL SSL_connect: SSL_ERROR_SYSCALL in connection to bootstrap.pypa.io:443`，则解决办法是：浏览器打开 `https://bootstrap.pypa.io/get-pip.py`，将文件复制下载到本地，然后执行本地的脚本文件。

参考链接：


- [Install Powerline MacOS](https://gist.github.com/itzderr/abdb2cdd795a23bc36e6a7838e388867)

### item2 终端安装

> 要先安装 python 环境，才能安装 Powerline。

参考链接：

- [iTerm2 + Oh My Zsh 打造舒适终端体验](https://github.com/github-repo-backup/iterm2-with-oh-my-zsh)

- [Install Powerline MacOS](https://gist.github.com/itzderr/abdb2cdd795a23bc36e6a7838e388867)
