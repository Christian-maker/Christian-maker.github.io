# wget
## 安装wget
### 简介
> wget 是一个从网络上自动下载文件的自由工具，支持通过 HTTP、HTTPS、FTP 三个最常见的 TCP/IP协议 下载，并可以使用 HTTP 代理。"wget" 这个名称来源于 “World Wide Web” 与 “get” 的结合。
### 安装
> 安装wget，可以使用brew安装，或者使用下面的命令安装：
```bash
$ brew install wget
```
> 也可以使用官方文件直接安装：

1. 下载 [wget](https://www.gnu.org/software/wget/wget.html)
2. 解压
3. 安装
```
$ tar xvf wget-1.19.4.tar.xz
$ cd wget-1.19.4
$ ./configure
$ make
$ make install
```

### 使用
1. 安装完成后，需要在系统中添加环境变量，可以通过以下命令添加：
```
$ export PATH=$PATH:/usr/local/bin
```
2. 在终端中运行 wget 命令，可以下载文件：
```
$ wget http://www.baidu.com
```


