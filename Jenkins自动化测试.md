# Jenkins自动化测试

一个持续集成的基本原则是构建应该是可验证的。你必须能够客观地确定一个特定的构建是否准备就绪构建过程的下一个阶段，最便捷的方式做到这一点是使用自动化测试。如果没有适当的自动化测试，会发现自己不得不保留许多手动生成工件，这几乎是在持续集成测试。下面的例子演示了如何使用Selenium运行自动化的Web测试。

**第1步** - 进入管理插件。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-15123011423R54.jpg)

**第2步**- 找到 Hudson Selenium 插件并选择安装。重新启动 Jenkins 实例。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230114300C4.jpg)

**第3步** - 转到配置系统。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-15123011432J49.jpg)

**第4步 **- 配置硒服务器 jar，然后点击保存(Save)按钮。
![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230114402535.jpg)

注 - Selenium jar文件可下载SeleniumHQ：[点击下载Selenium](http://www.seleniumhq.org/download/)的独立服务器。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-15123011460H96.jpg)

**第5步** - 返回到仪表板，然后单击配置 (Configure) 选项 HelloWorld 项目。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230114635K1.jpg)

**第6步 **- 点击添加构建步骤，并选择“SeleniumHQ htmlSuite Run”选项。

![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230114F4436.jpg)

**第7步** - 添加必要的细节 selenium 测试。在这里，suiteFile是使用selenium IDE生成TestSuite。点击保存(Save)并执行构建。现在后生成将启动 selenium 驱动程序，并执行HTML测试。
![img](http://www.yiibai.com/uploads/tutorial/20151230/1-151230114IQ21.jpg)