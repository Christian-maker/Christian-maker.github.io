# adb
## 安装adb
一、前置条件

安装Java JDK，可以参考文章：https://blog.csdn.net/dou_being/article/details/105320962

二、下载安装Android SDK 或 Android Studio，下载地址：http://tools.android-studio.org/

三、配置环境变量

1、Windows系统环境变量配置

（1）在系统环境变量中新建变量名为adb，变量值为Android SDK的platform-tools文件夹和build-tools文件夹的路径

（2）在系统环境变量的path中，添加adb的home目录：`%adb%`

（3）验证adb是否安装成功，在cmd命令窗口输入：adb 或 adb version，如果有一串信息打印出来，表示安装成功

2、MacOS系统环境变量配置

（1）对于android studio而言，默认的adb路径为：~ /Library/Android/sdk/platform-tools，注意：路径中"~"代表的根目录指的是当前用户的目录，并非整个mac系统的根目录

（2）在终端输入：`open -e .bash_profile`，如下图配置adb环境

![](..%2F..%2F..%2Fphoto%2Fadb01.png)\
（3）添加完后，保存并关闭文件，然后在终端输入：`source .bash_profile`，更新文件

（4）然后在终端输入adb，出现一长串帮助说明，证明adb已经配置好了，如图
![](..%2F..%2F..%2Fphoto%2Fadb02.png)

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
* 
```
adb help
```