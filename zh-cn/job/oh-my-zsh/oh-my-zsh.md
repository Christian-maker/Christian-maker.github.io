# oh-my-zsh
## ohmyzsh介绍
> 具有强大的可定制的特点，支持许多插件,补全功能也强大很多.但是却配置起来十分的麻烦，但有了oh-my-zsh之后，一切变得简单起来。

github地址：https://github.com/ohmyzsh/ohmyzsh
## ohmyzsh安装
### curl 安装
GitHub:
```
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
Gitee ( 国内镜像 )
```
sh -c "$(curl -fsSL https://gitee.com/mirrors/oh-my-zsh/raw/master/tools/install.sh)"
```

## oh-my-zsh插件
### oh-my-zsh-git
> 这个是装好oh-my-zsh就默认已经开启的

查看所有的git命令alias
```
$ ~/.oh-my-zsh/plugins/git/git.plugin.zsh
```
### oh-my-zsh-z
> 这个是oh-my-zsh默认就装好的，需要自己开启。还有一个autojump的插件和z功能差不多，autojump需要单独装，
如果z插件历史记录太多，并且有一些不是自己想要的，可以删除

### oh-my-zsh-autosuggestions
> 非常好用的一个插件，会记录你之前输入过的所有命令，并且自动匹配你可能想要输入命令，然后按→补全[>>项目地址](https://github.com/zsh-users/zsh-autosuggestions)
```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

```
plugins中别忘了添加上zsh-autosuggestions：
```
plugins=(
    zsh-autosuggestions
)
```

### oh-my-zsh-autojump
> 实现目录间快速跳转，想去哪个目录直接 j + 目录名(甚至不用输全)，不用在频繁的 cd 了[>>项目地址](https://github.com/wting/autojump)

brew 安装
```
brew install autojump
```
修改 `~/.zshrc` 文件，添加到plugins配置列表并在尾部追加如下内容：
```
[ -f /usr/local/etc/profile.d/autojump.sh ] && . /usr/local/etc/profile.d/autojump.sh
```
plugins中别忘了添加上autojump：
```
plugins=(
 autojump
)
```
### zsh-syntax-highlighting
>zsh-syntax-highlighting 插件为 shell zsh 提供语法高亮显示。当命令在 zsh 提示符下输入到交互式终端时，它可以突出显示命令。这有助于在运行命令之前检查命令，特别是捕获语法错误。[>>项目地址](https://github.com/zsh-users/zsh-syntax-highlighting)
#### 推荐使用HomeBrew进行安装：
brew安装
```
brew install zsh-syntax-highlighting
```
在 ～/.zshrc 尾部，插入一行：
```
source /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
```
生效配置
```
source ~/.zshrc
```
## iterm2
> 推荐一个好用的终端 iterm2，主要是花里胡哨好看。\
什么是iTerm2?\
iTerm2是默认终端的替代品，也是目前Mac系统下最好用的终端工具，集颜值和效率于一身。

先看看效果图：\
<img src="photo/iterm2.jpg" width=671 height=370 alt ="iterm2"> 

**觉得好看的可以安装以下教程设置，其他主题方法类似。**
### 调整Status Bar
>  将iTerm2自带theme修改为Minimal （ Preferences-Appearance-General-Theme ） 以达到顶栏沉浸式的效果.

可以在Profiles选项卡，Session页面最底部看到开启选项。Status bar enabled 选项，勾选上即可打开。点击右边的 Configure Status Bar 按钮可设置显示的内容。\
可以看到能显示的内容非常多，把上方要显示的内容拖动到下方 Active Components 区域即添加。\
在Preference页面中点击Appearance选项卡，可以设置Status bar的位置，修改 Status bar location，我这里改到Bottom底部

<img src="photo/iterm2-01.png" width=671 height=370 alt ="iterm2-01"> 

#### Status bar效果：
<img src="photo/iterm2-02.png"  alt ="iterm2-02"> \
显示的内容也可以自己调节：

<img src="photo/iterm2-03.png" width=671 height=370 alt ="iterm2-03"> 

### 更改配色(可选)
我比较喜欢 Dracula 配色方案，包括VS Code使用的都是这个配色方案。\
https://draculatheme.com/iterm/\
解压后更换 Preferences-Profiles-Color-Color ——> Presets-Import

### 设置zsh主题
<font size=4>配置主题：</font>

只需要修改 .zshrc 文件中的 ZSH_THEME="xx" 属性即可。\
我目前使用的主题是：spaceship\
按照github项目说明中的方法配置即可，或者参考本文下面的主题配置

<font size=4>下载主题文件：</font>
```
git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1
```
<font size=4>创建软连接</font>
```
ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
```
<font size=4>修改zsh配置</font>
```
vim ~/.zshrc
```
<font size=4>修改主题</font>
```
ZSH_THEME="spaceship"
```
<font size=4>重启zsh</font>
```
source ~/.zshrc
```
<font size=4>然后就是主题的一些配置，配置说明参考这个文件：</font>
```
https://github.com/denysdovhan/spaceship-prompt/blob/master/docs/Options.md
```
<font size=4>我的配置</font>
设置显示时间
```
SPACESHIP_TIME_SHOW="true"
```
设置显示用户名，并改用户名颜色为猛男粉
```
SPACESHIP_USER_SHOW="always"
SPACESHIP_USER_COLOR="212
```