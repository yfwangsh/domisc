# domisc
## hidden service
如何搭建自己的暗网站点

我们都知道暗网，知道tor。那我们知道，暗网最重要特性的就是匿名性，在那个地方，谁也不知道谁。那我们在那里面该如何搭建属于自己的网站呢？

操作系统：debain9

更新系统：apt-get update && apt-get upgrade
安装tor：apt-get install tor
安装nginx：apt-get install nginx

安装完之后，编辑tor配置文件
/etc/tor/torrc

把下面两条注释掉
HiddenServiceDir /var/lib/tor/hidden_service/
HiddenServicePort 80 127.0.0.1:80

然后启动tor，当然，nginx服务也要启动的，如果没有安装错误的话。
会在/var/lib/tor/hidden_service/这个目录生成hidden_service文件，打开有两个文件，其中hostname就是你的onion域名地址的文件，用tor浏览器访问即可。

## 移动资产发现
### APP
七麦：同开发者 https://www.qimai.cn/andapp/samePubApp/appid/6966742

