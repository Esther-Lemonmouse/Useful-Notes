# 如何减少50G的Docker占用空间
1. 使用`docker system df`可以查看占用的空间

2. 使用`docker system prune`清理缓存、已关闭的容器，无用的数据卷等等

3. 如果发现占用空间依然很大的话，请参考[How to Shrink a WSL2 Virtual Disk](https://stephenreescarter.net/how-to-shrink-a-wsl2-virtual-disk/)，将目标虚拟机的目录改为`C:\Users\<USERNAME>\AppData\Local\Docker\wsl\data\ex4.vdhx`即可。