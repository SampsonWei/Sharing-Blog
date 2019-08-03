@[TOC](使用IntelliJ idea—IDEA配置Go语言开发环境)
本文中将说明在`Windows 10`环境下使用**IDEA**来配置Go语言开发环境。
具体步骤如下

### 1.Go语言安装包下载

进入[Go语言官网](https://golang.org/dl/) ，选择合适的版本下载。
![go语言官网](https://img-blog.csdn.net/20181014153539704?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0tvcmVuX1dlaQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
等待下载完成。之后点击安装。

软件默认安装位置是`C:\Go`，大家可以根据自己使用习惯选择安装位置，方便用于环境变量配置。
###  2.Go语言环境变量配置
安装完成后，进入Windows环境变量配置环节。
具体添加`GOPATH`，此处的`GOROOT`路径为安装包位置。
![在这里插入图片描述](https://img-blog.csdn.net/20181018111908276?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0tvcmVuX1dlaQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
![在这里插入图片描述](https://img-blog.csdn.net/2018101811173762?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0tvcmVuX1dlaQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
点击**确认**完成。
为了确保正确安装，可进入终端窗口输入以下命令查看`Go`的版本号。

`go version`

![在这里插入图片描述](https://img-blog.csdn.net/20181014155156911?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0tvcmVuX1dlaQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
###  3.IDEA配置——添加Go插件
之后进入本地IDE——**IDEA**
点击进入`Plugins`，选择`Android Support`，点击`Browse repositories`。
![在这里插入图片描述](https://img-blog.csdn.net/20181014155738349?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0tvcmVuX1dlaQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
弹出`Browse`框后，点击选择`Manage repositories`。
![在这里插入图片描述](https://img-blog.csdn.net/20181014160423788?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0tvcmVuX1dlaQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
添加源地址，方便以后函数调用
`https://plugins.jetbrains.com/plugins/alpha/5047`
![在这里插入图片描述](https://img-blog.csdn.net/20181014160747597?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0tvcmVuX1dlaQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
之后搜索`Go`
![](https://img-blog.csdn.net/20181014155641805?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0tvcmVuX1dlaQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
此图片中我的已经安装，大家会看到`Install`按钮，点击安装，完成后**重启IDEA**。
![在这里插入图片描述](https://img-blog.csdn.net/20181014155924470?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0tvcmVuX1dlaQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

###  4.新建Go项目。
重启**IDEA**后，进入`Settings`界面设置`GOROOT`。
`GOPATH`需要设置为本项目
![在这里插入图片描述](https://img-blog.csdn.net/20181014161108126?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0tvcmVuX1dlaQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
点击确认之后。新建第一个`Go`项目文件`Hello`。（当然要建立在一个`package`下）
![在这里插入图片描述](https://img-blog.csdn.net/20181014161325344?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0tvcmVuX1dlaQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
```go
package main

import "fmt"

func main() {
	fmt.Printf("hello, world\n")
}
```
输入之后运行代码，出现` hello, world`

==**注意**==： `package main`是必须的，而且必须为`main`，负责编译报错。