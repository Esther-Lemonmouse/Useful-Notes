# Pycharm Professional自用远程开发



## Part 1: ssh+SFTP实现访问远程代码库并配置远程Python解释器

~~小破电脑炼丹的小诀窍，虽然我电脑不行，但我有服务器啊！~~

> **准备工作**
>1. Pycharm Professional
>2. 一台远程主机 (已经安装好python)

- **Step 1**: 打开Pycharm开始页面，依次点击 “自定义->所有设置->构建、执行、部署”
<这里大概将来会插英文版的图吧>

- **Step 2**: 选择“部署”，在配置页面中添加新的SFTP协议。
<这里大概将来会插英文版的图吧>

- **Step 3**: 在配置页面的ssh配置中点击 “...”，添加新的ssh配置，依次填入远程的主机ip，端口，远程主机用户名，密码。确认测试连接成功。
<这里大概将来会插英文版的图吧>

- **Step 4**: 建议将根路径设置在根目录，以便于将来的开发管理。

<这中间其实还有其他步骤（比如最关键的配置解释器这里），但是我现在不想写了，希望我以后还会想起来填坑吧>

完成~


## Part 2: Docker Desktop for Windows实现环境隔离式开发

~~炼丹的进化路线 (大概): Python->Anaconda->Miniconda->Docker~~

> **准备工作**
> 1. Pycharm Professional (安装了Docker相关插件)
> 2. Docker Desktop for Windows (确保Docker在配置时正在运行)
> 3. *已经配置好Python解释器的Container

*: 解释器路径很重要，我目前就卡在这里了

正式部分咕咕咕了，官方文档写得很好 (其实是因为现在我还不会)。Jetbrains的官方文档如下 (内含ssh，wsl，docker等等的远程解释器配置方法，便于食用)。

[Docker | Pycharm](https://www.jetbrains.com.cn/help/pycharm/docker.html)


参考资料:
知乎SFTP参考: <https://zhuanlan.zhihu.com/p/37361332>