[toc]

# Linux_目录

## Linux_目录结构

> 1. Linux 的文件系统，是采用级层式的树状目录结构。在此结构中，最上层是根目录“/”，然后在此目录下再创建其他的目录。
>
>     ==在 Linux 世界里，一切皆文件。==

### 具体目录结构

- ==/bin==(/usr/bin、/usr/local/bin)
    是 Binary 的缩写，这个目录存放着*最经常使用的*命令。
- <span style="color:red">/sbin</span>(/usr/sbin、/bsr/local/sbin)
    s 是 Super User 的意思，这里存放着*系统管理员使用的*系统管理程序。
- ==/home==
    存放普通用户的主目录，在 Linux 中，每个用户都有一个自己的目录，一般该目录名是以用户的账号命名。
- ==/root==
    该目录为系统管理员，也被称为超级权限者的用户主目录。
- <span style="color:red">/lib</span>
    系统开启所需要最基本的动态连接共享库。
    其作用类似于 Windows 里的 dll 文件，几乎所有的应用程序都需要用到这些共享库。
- <span style="color:red">/lost+found</span>
    这个目录一般情况下是空的，当系统非法关机后，这里就存放了一些文件。
- ==/etc==
    所有的系统管理所需要的配置文件和子目录。
    比如：安装 MySQL 数据库 my.conf
- ==/usr==
    这是一个非常重要的目录。
    用户的很多应用程序和文件都放在这个目录下，类似与 Windows 下的 program files 目录。
- ==/boot==
    存放的是启动 Linux 时，使用的一些核心文件，包括一些连接文件以及镜像文件。
- <span style="color:red">/proc</span>
    这是一个虚拟的目录，他是系统内存的映射，访问这个目录来获取系统信息。
- <span style="color:red">/srv</span>
    service 的缩写，该目录存放一些服务启动后需要提取的数据。
- <span style="color:red">/sys</span>
    这是 Linux2.6 内核的一个很大的变化。
    该目录下安装了 2.6 内核中新出现的一个文件系统 sysfs。
- <span style="color:red">/tmp</span>
    这个目录是用来存放一些临时文件的。
- <span style="color:red">/dev</span>
    类似于 Windows 的设备管理器，把所有的硬件用文件的形式存储。
- ==/media==
    Linux 系统会自动识别一些设备。如：U盘、光驱等。
    当识别后，Linux 会把识别的设备挂载到这个目录下。
- ==/mnt==
    系统提供该目录，是为了让用户临时挂载别的文件系统的。
    我们可以将外部的存储挂载在 /mnt/ 上，然后进入该目录，就可以查看里面的内容了。
    d:/myshare
- <span style="color:red">/opt</span>
    这是给主机额外安装软件所摆放的目录。
    如：安装 Oracle 数据库，就放在该目录下。默认为空。
- ==/usr/local==
    这是另一个给主机额外安装软件所摆放的目录。
    一般是通过编译源码方式安装的程序。
- ==/var==
    这个目录中，存放着在不断扩充着的东西，习惯将经常被修改的目录放在这个目录下。
    包括各种日志文件。
- <span style="color:red">/selinux</span>
    selinux 是一种安全子系统，它能控制程序只访问特定文件，有三种工作模式，可以自行设置。