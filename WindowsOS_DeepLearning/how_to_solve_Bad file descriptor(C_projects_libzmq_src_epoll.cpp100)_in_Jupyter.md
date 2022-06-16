# 我的Jupyter Notebook咋老崩？
## ——问题 _Bad file descriptor (C:\projects\libzmq\src\epoll.cpp:100)_ 的解决方案

1. Uninstall your package _pyzmq_ in your environment.
    ```
    pip uninstall pyzmq
    ```

2. Reinstall a lower version _pyzmq_ (e.g. 19.0.2).
    ```
    pip install pyzmq==19.0.2   #or pip3
    ```

3. Try to restart Jupyter Notebook.

这个问题的成因~~许是Jupyter的更新速度跟不上 _pyzmq_ 这个包的版本更新斯必得罢。应该是兼容性问题，回退版本可解~~是电脑用户名不是英文的缘故，重装系统可解。

感谢博客园老兄提供的解决方案~