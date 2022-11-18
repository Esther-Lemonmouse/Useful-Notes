# Enable Hibernate Function on Ubuntu22.04 LTS

~~在大哥的carry下~~给电脑安装了Ubuntu系统以后，某一天我突然开始眼馋起了Windows系统自带的休眠功能，并且想在Ubuntu上实现相同功能~~要打游戏的嘛~~。于是浅浅尝试了一下，现将步骤记录于此。


## 重要参考网页

因为基本都是靠着教程嗯搞出来的，教程里已经说明的部分我就不记录了。
<a id="basic_tutorial">
+ 保姆级攻略(grab启动可以直接参考): <https://ubuntuhandbook.org/index.php/2021/08/enable-hibernate-ubuntu-21-10>
</a> 

+ ArchWiki的说明和教程(更详细，但是不太好懂): <https://wiki.archlinux.org/title/Power_management/Suspend_and_hibernate>

+ 通过直接修改`/swapfile`增加交换空间大小: <http://t.csdn.cn/tsD7M>
    <a id="swap">
    > 补充阅读: [交换空间的N种写法，你知道吗？](https://wiki.archlinux.org/title/Swap)
    </a>


## 背景

此处列出我的电脑配置

+ 系统：Ubuntu22.04 LTS

+ 启动引导: rEFInd (grab被隐藏起来了，但并未禁用)

+ 交换空间: swapfile类型，初始2G


## 步骤

+ 增加swap大小。为了以防万一，设置的swap空间需要略大于RAM。增加的方式可以参考[swap的N种写法](#swap)。我直接修改了`/swapfile`的大小并设成了20G。

+ 参照[新手教程](#test)获取swap的UUID。

+ 参考修改grub内核参数的方法，修改rEFInd配置文件(大概位于`/boot/refind_linux.conf`里)
```bash
# resume_offset适用于使用swapfile的情况，具体获取方式同样参考新手教程
# 貌似修改第一行标准模式的内核参数就行了
"Boot with standard options"  "root=UUID=xxx-xxx-xxx-xxx-xxx ro quiet splash  resume=UUID=xxx-xxx-xxx-xxx-xxx resume_offset=yyy vt.handoff=7"
# 原始设置: "root=UUID=xxx-xxx-xxx-xxx-xxx ro quiet splash vt.handoff=7"
"Boot to single-user mode"    "root=UUID=xxx-xxx-xxx-xxx-xxx ro quiet splash vt.handoff=7 single"
"Boot with minimal options"   "ro root=UUID=xxx-xxx-xxx-xxx-xxx"
```

Mission Complete!