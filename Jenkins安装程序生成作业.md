# Jenkins安装程序生成作业

在这个练习中，我们将在Jenkins建立一份作业来执行一个简单的 HelloWorld 应用程序，构建和运行Java程序。打开网址：<http://localhost:8080/jenkins>

**第1步**- 转到Jenkins 仪表板，然后单击新建项目(New Item)

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230112552T0.png)

****

**第2步** - 在接下来的屏幕上，输入项目名称，在这种情况下，我们把它命名为：HelloWorld。选择“Freestyle project option”

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-15123011260H07.png)

**第3步 **- 下面的屏幕会在其中您可以指定作业的详细信息。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230112625629.png)

**步骤4** - 我们需要指定需要被建立的文件的位置。在这个例子中，我们假设一个本地的SVN仓库(D:\worksp\yiibai.com\jenkins)已经建立，其中包含一个“HelloWorld.java”文件。因此，向下滚动，点击 SVN 的选项，并输入本地 SVN 仓库的URL。

注 - 如果存储库，如果托管在Github上，你也可以在这里输入库的URL。除了这一点，你需要点击添加按钮的凭据，用户名和密码添加到GitHub的资源库，以便可以从远程仓库拾取代码。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230112A1639.png)

添加SVN用户名和密码：

**第5步** - 现在到生成部分，然后单击添加构建步骤→执行Windows批处理命令

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230112HL10.png)

**第6步** - 在命令窗口中，输入以下命令，然后单击保存按钮。

```
Javac HelloWorld.java
Java HelloWorld

```

**![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230112J91X.png) 第7步** - 保存后，可以在构建单击立即选项，查看是否已成功定义了工作。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230112SCO.png)

**第8步** - 一旦构建计划，它将运行。下面 “Build history” 部分显示构建正在进行中。

一旦构建完成后，构建的状态将显示，如果构建成功与否。在我们的例子，下面的生成已成功执行。点击在构建历史的＃1，弹出构建的细节。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230112UHa.png)

**第9步** - 点击控制台输出链接查看构建的细节(如果程序出错，可能需要多尝试多构建几次)

除了上面的步骤目前只有这么多的方法来创建构建工作，可用的选项还有很多，这是什么 Jenkins 这样一个梦幻般的连续部署工具。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230112914927.png)