# Useful WSL + Docker Resources

- **配置WSL2后端支持的docker。**
    非常好用！从此Windows系统上跑Linux不是梦！安装完container之后还支持GPU加速！朋友，不来试试吗~
    官方文档戳 [WSL 2 上的 Docker 远程容器入门](https://docs.microsoft.com/zh-cn/windows/wsl/tutorials/wsl-containers)。本教程相关页面 [适用于 Linux 的 Windows 子系统文档](https://docs.microsoft.com/zh-CN/windows/wsl/) 内容更全面，就是一整个手把手教人使用WSL的操作。

- **配置WSL2 Docker的GPU支持**
    1. 确认是否是NVIDIA支持的加速类型

    2. 确认**本地主机** (不是wsl) 正确安装了最新版的显卡驱动。可以在命令行以nvidia-smi命令检查。

    3. [Docker 文档：将 Docker Desktop 与 WSL 2 配合使用的最佳做法](https://docs.docker.com/desktop/windows/wsl/#gpu-support)
    按照上述文档说明运行完简短测试 (建议在WSL虚拟机中运行)。控制台打印出的信息会与文档中的类似。

    4. 安装nvidia-docker
    + NGC有提供比较完备的image，高度集成。<https://catalog.ngc.nvidia.com/containers>
    + (自用方法) 使用Docker Hub上由NVIDIA发布的image+Dockerfile(还没写出来)生成新的container。<https://hub.docker.com/>
    **Tips:** 注意在生成容器时使用关键字`--gpus all`，否则前面所做的一切都白搭 ~~by删了不知道多少号的菜鸡~~

    5. 在生成好的container bash中运行nvidia-smi，如果有正确输出则代表大功告成，可以安心享受深度学习开发环境啦~

## 一个Pytorch开发环境的示例（待续）