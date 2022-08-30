[toc]

# VM 和 Linux 的安装

> ​	学习 Linux 需要一个环境。我们需要一个虚拟机，之后在虚拟机上安装一个 CentOS 系统来学习。
>
> ​	1、先安装 virtual machine 15.5
> ​	2、再安装 Linux(CentOS 7.6 / CentOS 8.1)



## VMWare 16 下载

- 官方地址：<https://www.vmware.com/cn.html>
- 其他地址：<https://www.nocmd.com/windows/740.html>

## CentOS 下载

- CentOS 7.6：[CentOS-7-x86_64-DVD-1810.iso](http://mirror.nsc.liu.se/centos-store/7.6.1810/isos/x86_64/CentOS-7-x86_64-DVD-1810.iso)
- CentOS 8.1：[CentOS-8.1.1911-x86_64-dvd1.iso](https://vault.centos.org/8.1.1911/isos/x86_64/CentOS-8.1.1911-x86_64-dvd1.iso)(迅雷下载)

## CentOS 安装

1. 使用 VMware Workstation Pro 16 创建一个虚拟机。
2. 开始安装 CentOS 7.6。
    *随机生成复杂密码：https://suijimimashengcheng.bmcx.com/*
3. CentOS 安装难点 - 网络连接方式(理解)

> 1、桥接模式：虚拟系统可以和外部系统通讯，但是容易造成 IP 冲突。
>
> 2、NAT 模式：网络地址转换模式。虚拟系统可以和外部系统通讯，且不造成 IP 冲突。
>
> 3、主机模式：独立的系统。不与外部进行联系。

4. 分区：
   - /boot(启动分区)：1G-标准分区-ext4
   - swap(交换分区)：2G-标准分区-swap
   - /：剩下内存-标准分区-ext4
