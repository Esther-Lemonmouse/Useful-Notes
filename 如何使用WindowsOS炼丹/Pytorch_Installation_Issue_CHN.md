# 我的Pytorch咋安不上呢（国内）？

使用说明：本文可以解决conda环境下的安装问题，pip我不晓得，不过应该本质差不多。
pip记得用Linux操作系统。

1. 在conda设置里添加清华大学镜像源。[tutorial点我](https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/)

2. 去Pytroch官网，选好对应的版本，拷贝命令到conda里。不要相信网上的把 -c pytorch去掉之类的建议，原样拷贝即可。conda会自动重定向到清华源。


3. 打开Python控制台，输入以下命令查看版本：
    ```Python
        import torch
        print(torch.__version__)
    ```
    如果导入成功就说明已经安好辣~撒花！