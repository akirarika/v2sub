# v2ray-subscriber

一个适用于 v2ray 的服务器代理订阅器，可以帮助你从订阅链接中获取、测试和切换代理服务器。仅在 Arch Linux 下有过测试。

## 使用方式

本脚本使用 Python3 编写，通过直接调用 v2ray 命令及直接更改 v2ray 的配置文件来实现。所以，您需要安装 python3 跟 v2ray 才能使用。

使用本脚本很简单，以 root 用户身份执行即可。`sudo ./v2sub`

**另：** 本脚本以过程式编程书写，而且 config.json 的内容都是硬编码在脚本内的，执行本脚本还会覆盖您在 /etc/v2ray 中的 config.json 文件。所以如果您想修改默认端口等配置，您可以直接编辑本脚本文件，修改里面 config.json 的内容~~或者去自己写~~。

当您使用过后，您可以将本脚本的软连接添加至 `/usr/bin` 或者其他的什么地方，这样您在想换代理服务器时，只需要在终端敲 `v2sub` 就好了。

## 在 Arch Linux 下安装 v2ray
```
sudo pacman -S v2ray
systemctl enable v2ray.service
```
