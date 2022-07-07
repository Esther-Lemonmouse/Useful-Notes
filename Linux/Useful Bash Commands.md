# 每天一个Bash歪门邪道小技巧

+ 查看Linux磁盘上可用空间个分区占比
```bash
df -h
```

+ 查看当前目录的使用空间大小
```bash
du -sh
```

+ 本地和远程主机互传文件 (夹)
```bash
# file
scp [FILE_DIRECTORY] [DESTINATION_DIRECTORY]
# folder
scp -r [FOLDER_DIRECTORY] [DESTINATION_DIRECTORY]
# remote directory: USERNAME@IP_ADDRESS:REMOTE_DIRECTORY
```

+ 远程服务器访问
```bash
ssh USERNAME@IP_ADDRESS
```

+ 查看磁盘详细进程 (所有)
```bash
ps -auxf
```

+ 查看服务器GPU当前状态 (需安装gpustat)
```bash
gpustat
```

+ 查看Nvidia显卡硬件性能
```bash
nvidia-smi
```

+ 保持进程不挂断运行
```bash
nohup COMMAND
```

+ 提升进程优先级 (防止后台运行时被挤掉)
```bash
# value range: 0-19
nice -n VALUE COMMAND
```

+ 查看硬盘进程优先级
```bash
top
```

+ 添加Ubuntu系统的中文支持
```bash
apt install x11-apps
apt install locales xfonts-intl-chinese fonts-wqy-microhei
# 后面好像还有别的步骤，我就不写了，到时候查吧，反正这么搞完Ubuntu就能识别中文了
```