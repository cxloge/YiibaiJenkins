# Jenkins持续部署

Jenkins提供很好的连续部署和交付的支持。看一下部署任何软件开发的流程，将如下图所示。
![img](http://www.yiibai.com/uploads/tutorial/20151230/1-1512301546405b.jpg)

连续部署的主要部分，是确保其上面所示的整个过程是自动化的。Jenkins实现所有这些是通过各种各样的插件，其中一个是“Deploy to container Plugin”，这个在较早的教程中有介绍过了。
![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230154F6127.jpg)

有可用的插件，实际上可以在连续部署过程中以图形表示。但首先，让我们创建 Jenkins 的另一个项目，这样我们就可以看到它是如何工作的。

让我们创建一个简单的项目，它模拟了QA阶段，并执行 HelloWorld 应用程序的测试。

**第1步** - 转到 Jenkins 仪表板，然后单击新建项目。选择“Freestyle project”，并输入该项目名称为“QA”。点击 OK 按钮创建项目。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230154J5Q6.jpg)

**第2步** - 在这个例子中，我们保持简单，只用这个项目来对 HelloWorld 应用程序执行测试计划。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230154Q4264.jpg)

因此，我们的项目 QA 现在安装。可以做一个构建，看它是否正确构建。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230154S0927.jpg)

**第3步** - 现在转到 Hello World 项目，并单击配置(Configure)选项

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230154UM13.jpg)

**第4步**- 在项目结构中，选择“Add post-build action”，并选择“Build other projects”：

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-15123015491V92.jpg)

**第5步** - 在“Project to build”部分中，输入QA以建立项目名称。可以保留该选项为默认的“Trigger only if build is stable”。点击保存按钮。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-1512301549462D.jpg)

**第6步** - 建立 HelloWorld 项目。现在如果你看到控制台输出，也将看到 HelloWorld 项目成功建成后，QA项目的构建也将发生。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230155020401.jpg)

**第7步**- 现在安装Delivery pipeline插件。转到 Manage Jenkins → Manage Plugin’s. 在可用的选项卡中，搜索“Delivery Pipeline Plugin”。点击安装不重新启动。完成后，重新启动 Jenkins 实例。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230155046204.jpg)

**第8步** - 要查看Delivery pipeline 动作，在Jenkins仪表板，单击选项卡旁边的 ‘All’ 选项卡上的+符号。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230155105429.jpg)

**第9步** - 输入视图名称并选择'Delivery Pipeline View“ 选项。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-15123015512B28.jpg)

第10步 - 在下一屏幕，可以保留默认选项。也可以更改以下设置 −

- 确保选择“Show static analysis results”被选中。
- 确保选择“Show total build time”被选中。
- 对于最初的工作 - 输入 HelloWorld 项目作为应该建立的第一个作业。
- 为管道(Pipeline)输入名字
- 单击确定(OK)按钮。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230155202Z1.jpg)
现在，将看到整个管道的一个大的视图，其中有整个管道每个项目的状态。
![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230155305I2.jpg)

另一个著名的插件是构建管道的插件。让我们来看看它。

**第1步** - 进入Manage Jenkins → Manage Plugin。在可用的选项卡中，搜索“Build Pipeline Plugin”。点击安装不重新启动(Install without Restart)。完成后，重新启动 Jenkins 实例。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-1512301553302Q.jpg)

**第2步** - 要查看生成管道在动作中，在Jenkins 仪表板，单击选项卡旁边的“All”选项卡上的+符号。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-1512301553533S.jpg)

**第3步 **- 输入视图一个名称并选择“Build Pipeline View”选项。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230155416109.jpg)

**第4步** - 接受默认设置，只是选择初始工作，确保进入 HelloWorld 项目的名称。点击确定(Ok)按钮。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-1512301554404H.jpg)

现在，将看到整个管道的一个大的视图，可看到整个管道每个项目的状态。
![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230155503S7.jpg)