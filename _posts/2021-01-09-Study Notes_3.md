---
layout: page
title: dns域名解析，泛域名解析（成功案例）
excerpt_separator: "<!--more-->"
categories:
     - 学习笔记
---

# 篇三
## title: dns域名解析，泛域名解析（成功案例）
#### 一个根域里面有两个主机就是称为泛域名，两个网站都是指向了同一个 IP，也就是不同的主机名可以指向不同的网站目录，而 FTP 就是只做在另外一个地址上面，在 DNS 里面配置使用客户端来进行安装
有很多同学可能在liunx里面配置dns域名解析失败了，现在给大家分享成功案例，以下一些要注意的点。
<!--more-->
账号：182.254.192.28
密码：不告诉你

配置目标为：

```
ftp.zxpzxp.cn 182.254.192.28
mail.zxpzxp.cn 118.126.105.5
www.zxpzxp.cn 182.254.192.28
```
登录putty
1.安装DNS域名系统：
```
yum -y install bind  
```
2.修改主配置文件：
```
vim /etc/named.conf
```

3.创建域名：
 ```
vim /etc/named.conf
```

按以上格式填写自己的域名
```
zone "zxpzxp.com."IN{
type master;
file "zxpzxp.com.zone";
};
```
在需要复制的第一行，未启动i进行编辑的时候，按下4，yy进行复制，然后按i进行编辑，移动到需要粘贴的地方按下p进行复制。
4.创建正向区域数据库文件
```
cp -p named.localhost nfu.edu.cn.zone
```

修改自己域名的文件
5、修改正向区域数据库文件
```
vim /var/named/zdnf.com.zone
```

6、重启服务：(在确保上面步骤正确的情况下进行，不然会报错，报错一般是因为代码问题，一个标点符号缩进都不能有问题)
```
systemctl restart named
```

7.在客户端设置域名服务器的地址
```
vim /etc/resolv.conf
nameserver 182.254.192.28
```

8.	测试
（1）先在腾讯云上解析：（添加记录）要先进行域名的解析才能实现dns域名解析，不然ping不通。最后进行一个测试。


```
nslookup dns.zxpzxp.cn
```

```
nslookup mail.zxpzxp.cn
```


```
nslookup www.zxpzxp.cn
```
具体细节部分可以看莫师兄的，他的很详细
参考：https://www.jianshu.com/p/4c5af0e0b1e9
