# Jenkins Tomcat安装设置

以下为必须满足Jenkins Tomcat设置的先决条件。

## 第1步：验证安装Java

要验证Java安装，打开控制台并执行以下Java命令。

| OS      | 任务      | 命令              |
| ------- | ------- | --------------- |
| Windows | 打开命令控制台 | \>java –version |
| Linux   | 打开命令终端  | $java –version  |

如果Java已经正确地在系统上安装，那么你应该得到以下输出之一，这取决于您所使用的系统平台。

| OS      | 输出                                       |
| ------- | ---------------------------------------- |
| Windows | Java version "1.7.0_60"Java (TM) SE Run Time Environment (build 1.7.0_60-b19)Java Hotspot (TM) 64-bit Server VM (build 24.60-b09, mixed mode) |
| Linux   | java version "1.7.0_25"Open JDK Runtime Environment (rhel-2.3.10.4.el6_4-x86_64)Open JDK 64-Bit Server VM (build 23.7-b01, mixed mode) |

我们假设本教程的读者在学习本教程之前已经安装了 Java1.8 安装在他们的系统中。

如果您没有安装Java JDK，可以从链接下载： [Oracle官方网站](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html)

## 第2步：验证安装Java

设置JAVA_HOME环境变量设置指向安装在您的计算机上 Java 的基本目录位置。 例如，

| OS      | Output                                   |
| ------- | ---------------------------------------- |
| Windows | 设置环境变量 JAVA_HOME 为 C:\ProgramFiles\java\jdk1.8.0_60 |
| Linux   | export JAVA_HOME=/usr/local/java-current |

追加 Java 编译器的位置到系统路径的完整路径。

| OS      | 输出结果                                     |
| ------- | ---------------------------------------- |
| Windows | 附加字符串; C:\Program Files\Java\jdk1.8.0_60\bin 到系统变量PATH的尾端。 |
| Linux   | export PATH=$PATH:$JAVA_HOME/bin/        |

验证命令java版本，如上所述在命令提示符。

## 步骤3：下载Tomcat

Tomcat官方网站 [Tomcat](http://tomcat.apache.org/). 如果您单击给定链接，就可以链接到 tomcat 官方网站的首页上，如下图所示。
![img](http://www.yiibai.com/uploads/tutorial/20151229/1-1512291QQ2W0.jpg)

浏览到链接 <https://tomcat.apache.org/download-70.cgi> 获得下载 Tomcat 的程序包。
![img](http://www.yiibai.com/uploads/tutorial/20151229/1-1512291QTH91.jpg)

转到 ‘Binary Distributions’ 区块部分。下载 64 位 Windows 的 zip 文件。

然后解压缩下载 zip 文件的内容。

## 第4步：Jenkins和Tomcat安装

从以前下载的 Jenkis.war 文件并将其复制到 tomcat 的 webapps 文件夹中文件夹中。

现在，打开命令提示符。在命令提示符下，浏览到 tomcat7 文件夹所在的目录。浏览到此文件夹中的 bin 目录，然后在文件中运行 start.bat 

```
D:\worksp\yiibai.com\tomcat7\bin>startup.bat
```

当处理是完全没有严重错误，在命令提示符会输出以下行。

```
INFO: Server startup in 9468 ms
```

打开浏览器，打开链接- <http://localhost:8080/jenkins>。Jenkins 将启动并 Tomcat 上运行。
![img](http://www.yiibai.com/uploads/tutorial/20151229/1-1512291Q930103.png)