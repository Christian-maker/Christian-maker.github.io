## 安装adb
最简单的安装方法，直接下载Android studio \
下载地址：https://developer.android.google.cn/studio

## adb命令
#### 查看当前连接设备：
* 查看当前链接设备：
```angular2html
adb devices
```
* 如果发现多个设备：
```angular2html
adb -s 设备号 其他命令
```
#### adb安装应用和卸载：
* 安装apk应用
```angular2html
adb install 安装包路径
```
* 覆盖安装(-r 代表如果apk已安装，重新安装apk并保留数据和缓存文件)
```angular2html
adb install -r 安装包路径
```
* 卸载安装包
```angular2html
adb uninstall 包名package
```
#### 开启和关闭服务：
* 开启服务
```angular2html
adb start-server
```
* 关闭服务
```angular2html
adb kill-server
```
#### adb传输文件：
* 将电脑文件传输到移动端
```
adb push 电脑路径 移动端路径
```
* 将移动端文件传输到电脑
```
adb pull 移动端路径 电脑路径
```
#### 查看顶部Activity:
* windows环境下:
```
adb shell dumpsys activity | findstr "mFocusedActivity"
```
* Linux、Mac环境下：
```
adb shell dumpsys activity | grep "mFocusedActivity"
```
#### 查看手机端安装的所有app包名:
```
adb shell pm list packages
```
* 帮助
```
adb help
```