# brew
## 安装brew
### 一.执行brew官网命令安装brew
官网中复制下图中命令，在terminal中输入该命令，即：
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```
### 二.更换镜像源安装brew
* 将brew的install文件下载到本地。在terminal中依次输入如下命令
```
cd ~
curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install >> brew_install
```
* 修改install文件的镜像源。
    * 打开brew_install文件，terminal中执行命令 open ~/brew_install
    * 将brew_install文件中的
```
BREW_REPO = "https://github.com/Homebrew/brew".freeze
CORE_TAP_REPO = "https://github.com/Homebrew/homebrew-core".freeze
```
替换为：
```
BREW_REPO = "git://mirrors.ustc.edu.cn/brew.git".freeze
CORE_TAP_REPO = "git://mirrors.ustc.edu.cn/homebrew-core.git".freeze
```
无 CORE_TAP_REPO 的话，则不需要替换。然后按 Command+s (win用Ctrl)保存文件。
* 安装brew。terminal中执行如下命令
```
/usr/local/bin/ruby ~/brew_install
```
使用第二种方法有些会成功。但我使用了这种方法，还是下载慢，超时报错。此时此刻你脑海里可能会闪现一个念头：fq吧，没错，你的想法很正确。然后我就跑去购买了VPN，再次下载......

![](../../../photo/哭泣.jpg)

### 三.安装brew的终极方法（一）
以上两种方法均没有安装成功，然后查找资料，发现可能是公司内部网络有限速，于是使用第三种方法：
* 打开手机热点，mac电脑连接手机热点。
* 然后按照第一种方法，输入brew官网安装命令，你会发现下载速度很快，且安装成功~

![](../../../photo/意不意外？.jpg)

### 四，安装brew的终极方法（二）
今天同事推荐了一种不需要连手机热点的镜像安装方法。电脑终端输入如下命令：
```
/bin/zsh -c "$(curl -fsSL https://gitee.com/cunkai/HomebrewCN/raw/master/Homebrew.sh)"
```
按回车后，根据提示操作：输入镜像序号 --> 输入Y，回车等待brew安装完成即可。

## 卸载brew
卸载就比较方便了。
```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/uninstall)"

```

## brew使用介绍
### 常用命令
#### 1.安装和卸载
```
brew --version或者brew -v 显示brew版本信息
brew install <formula> 安装指定软件
brew unistall <formula 卸载指定软件
brew unistall <formula 卸载指定软件
brew list 显示所有的已安装的软件
brew search text 搜索本地远程仓库的软件，已安装会显示绿色的勾
brew search /text/ 使用正则表达式搜软件
```
### brew更多文档
* [brew手册页（命令文档）](https://docs.brew.sh/Manpage)
* [Homebrew 博客（有关重大更新的新闻）](https://brew.sh/blog/)
* [故障排除](https://docs.brew.sh/Troubleshooting)
* [安装brew](https://docs.brew.sh/Installation)
