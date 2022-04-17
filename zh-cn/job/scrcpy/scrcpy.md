# scrcpy
## 安装scrcpy
> scrcpy是一款Android设备投屏插件，支持投屏、录屏、截图、设备管理、设备连接、设备状态等功能。

在Mac上通过brew命令来安装scrcpy
```
brew install scrcpy
```

安装的时候可能会出错，参考[brew install not working on Mac (Catalina) #](https://github.com/Genymobile/scrcpy/issues/2247)，可先使用brew update 更新brew

## scrcpy使用
### 常用命令
*电脑投屏
```
scrcpy
```
* 手机通过电脑录屏(保存在终端当前的目录下)
```
scrcpy -r 文件名.mp4
```
* 轨迹球
```
scrcpy --show-touches
scrcpy -t
```


## scrcpy键盘操作
键盘控制投屏

描述 | 快捷键 
- | :-: 
切换全屏模式 | Command/Ctrl+f
点击手机电源 | Command/Ctrl+p
返回 | Command/Ctrl+b
返回到HOME | Command/Ctrl+h
多任务 | Command/Ctrl+s
滚动屏幕 | Command/Ctrl+←/→
更多操作 | 长按鼠标左键
显示最佳窗口 | Command/Ctrl+g
调节音量 | Command/Ctrl+上下键
关闭设备屏幕（保持投屏） | Command/Ctrl+0
将设备剪切板复制到计算机 | Command/Ctrl+c
讲计算机剪切板粘贴到设备 | Command/Ctrl+v

