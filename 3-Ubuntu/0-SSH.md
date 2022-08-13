[toc]

# SSH

## 概述

> SSH(Secure Shell)：由 IEIF 的网络工作小组(Network Working Group)所制定。SSH 为建立在应用层和传输层基础上的安全协议。
>
> SSH 是目前较可靠，专为远程登录会话和其他网络服务提供安全性的协议。常用于远程登录。几乎所有的 UNIX / Linux 平台都可以运行 SSH。
>
> 使用 SSH 服务，需要安装相应的服务器和客户端。客户端和服务器的关系：
> 	如果 机器A 需要被 机器B 所远程控制，那么 机器A 需要安装 SSH 服务器，机器B 需要安装 SSH 客户端。
>
> 与 CentOS 不一样，Ubuntu 默认没有安装 SSHD 服务(使用 netstat 指令查看：apt install net-tools)。因此，我们无法远程登录。