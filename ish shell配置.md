ish shell 使用的是 alphine linux 系统。

# 一、基础操作
ish shell 使用的是 apk 包管理器，常用操作如下：

* 安装软件 `apk add ···`
* 更新源`apk update ···`

换源：
```bash
sed -i 's/apk.ish.app\/v3.14-2023-05-19/mirrors.tuna.tsinghua.edu.cn\/alpine\/v3.14/g' /etc/apk/repositories
```

# 二、挂载 ios 的文件系统到 ish shell 中

先在 mnt 中创建一个目录用来与 ios 中的文件夹进行链接：
```bash
mkdir ./mint/ipad
```
然后进行链接：
```bash
mount -t ios p . /mnt/ipad
```
