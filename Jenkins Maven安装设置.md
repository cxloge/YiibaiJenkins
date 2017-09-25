# Jenkins Maven安装设置

如果没有学习过 Maven 的朋友，可以先了解 Maven教程，然后再进一步学习本教程文章。

## 第1步：下载和设置Maven

Maven的官方网站就是[Apache Maven](https://maven.apache.org/download.cgi)。如果点击给出的链接，就可以打开 Maven 的官方网站的首页，如下图所示。
![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230111015562.jpg)

浏览该网站，进入文件部分并下载链接二进制的 .zip 文件。
![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230111041336.jpg)

一旦文件被下载，解压缩文件到相关的应用程序文件夹。为了这个目的，Maven 的文件将被放置在 D:\worksp\yiibai.com\apache-maven-3.3.9

## 第2步：设置 Jenkins 和 Maven

在 Jenkins 仪表盘(主屏幕)，请在左侧菜单中选择管理 Jenkins。打开网址：<http://localhost:8080/jenkins>
![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230111111209.png)

然后，从右侧单击“Manage Jenkins”。
![img](http://www.yiibai.com/uploads/tutorial/20151230/1-15123011113A41.png)

再点击“Configure Sytem"，结果如下图所示：
![img](http://www.yiibai.com/uploads/tutorial/20151230/1-15123011115Ka.png)

在配置系统屏幕上滚动，直至看到 Maven 部分，然后点击“Add Maven'按钮。

取消选中“Install automatically”选项。

添加名称和设置 MAVEN_HOME 的位置。

然后，在屏幕的末尾点击“Save”按钮。
![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230111225411.png)

现在，可以创建一个‘Maven project’选项的作业。在Jenkins仪表盘，单击新建项目选项。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230111250V9.png)

完成后如下图所示：
![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230111304D9.png)