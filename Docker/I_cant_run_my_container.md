# I Cannot Run My Container!

一句话解答: **为什么不好好读官方文档，善用搜索功能呢？**

~~别骂了555~~

[Docker Documentation](https://docs.docker.com/) 我想要的一切，都在这里。

不过还是得说一下，怎么创建一个不会秒结束的container。运行以下命令就可以啦~
```shell
docker run -it IMAGE[:TAG|@DIGEST] bash
# 先不要尝试如下命令
# docker run -it --rm IMAGE[:TAG|@DIGEST] bash
```
image的结构为 `<repository_name>:<tag_name>`

这样它至少不会秒卒。