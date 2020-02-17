## 下载

### 下载地址

Go官方镜像站：https://golang.google.cn/dl/

Git官方下载地址：https://git-scm.com/downloads

### 版本的选择

Windows平台和Mac平台推荐下载可执行文件版，Linux平台下载压缩文件版。

*根据自己的操作系统来选择对应的版本。*

![1550814038938](https://github.com/Felixchen16/golang/blob/master/docs/pic/2.1.jpg?raw=true)

因为需要在github上下载各种go的插件，所以最好把Git也安装上。

![](https://github.com/Felixchen16/golang/blob/master/docs/pic/2.2.png?raw=true)

## 安装

### Windows安装

##### [观看安装配置视频讲解](https://www.bilibili.com "观看安装配置视频讲解")

此安装实例以 `64位win7` 系统安装 `go1.13.8.windows-amd64`和`Git-2.25.0-64-bit`为例。

将上一步选好的安装包下载到本地。

**配置GOPATH**

`GOPATH`是一个环境变量，用来表明你写的go项目的存放路径（工作目录）。

`GOPATH`路径最好只设置一个，所有的项目代码都放到`GOPATH`的`src`目录下。

按照操作视频的步骤安装配置即可。

**GOPATH在不同操作系统平台上的默认值**

|  平台   |   GOPATH默认值   |        举例        |
| :-----: | :--------------: | :----------------: |
| Windows | %USERPROFILE%/go | C:\Users\用户名\go |
|  Unix   |     $HOME/go     |  /home/用户名/go   |

同时，我们将 `GOROOT`下的bin目录及`GOPATH`下的bin目录都添加到环境变量中。

配置环境变量之后需要重启你电脑上已经打开的终端。（例如cmd、VS Code里面的终端和其他编辑器的终端）。

### Linux下安装

我们在版本选择页面选择并下载好`go1.13.8.linux-amd64.tar.gz`文件：

```bash
wget https://dl.google.com/go/go1.13.8.linux-amd64.tar.gz
```

将下载好的文件解压到`/usr/local`目录下：

```bash
mkdir -p /usr/local/go  # 创建目录
tar zxf go1.13.8.linux-amd64.tar.gz -C /usr/local/go  # 解压
```

如果提示没有权限，加上`sudo`以root用户的身份再运行。执行完就可以在`/usr/local/`下看到go目录了。

配置环境变量： Linux下有两个文件可以配置环境变量，其中`/etc/profile`是对所有用户生效的；`$HOME/.profile`是对当前用户生效的，根据自己的情况自行选择一个文件打开，添加如下两行代码，保存退出。

```bash
export GOROOT=/usr/local/go
export PATH=$PATH:$GOROOT/bin
```

修改`/etc/profile`后要重启生效，修改`$HOME/.profile`后使用source命令加载`$HOME/.profile`文件即可生效。 检查：

```bash
~ go version
go version go1.13.8 darwin/amd64
```

### Mac下安装

下载可执行文件版，直接点击**下一步**安装即可，默认会将go安装到`/usr/local/go`目录下。安装过程执行完毕后，可以打开终端窗口，输入`go version`命令，查看安装的Go版本。



## 目录结构

在进行Go语言开发的时候，我们的代码总是会保存在`$GOPATH/src`目录下。在工程经过`go build`、`go install`或`go get`等指令后，会将下载的第三方包源代码文件放在`$GOPATH/src`目录下， 产生的二进制可执行文件放在 `$GOPATH/bin`目录下，生成的中间缓存文件会被保存在 `$GOPATH/pkg` 下。

如果我们使用版本管理工具（例如Git）来管理我们的项目代码时，我们只需要添加`$GOPATH/src`目录的源代码即可。`bin` 和 `pkg` 目录的内容无需版本控制。

