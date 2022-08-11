[toc]

# 虚拟机操作

## 虚拟机克隆

> 	1. 方式一：直接拷贝一份安装好的虚拟机文件。
>  	2. 方式二：使用 VMware 的克隆操作。
>  	注意：克隆时，需要关闭 Linux 系统。

## 虚拟机快照

> 如果在使用虚拟机系统时（如 Linux），想回到原先的某一状态，也即是说担心可能有些误操作造成系统异常，需要回到原先某个正常运行的状态，VMware 也提供了这样的功能，叫做*快照管理*。
>
> 应用实例：
>
> 	1. 安装好系统后，先做一个快照A
> 	1. 进入到系统，创建一个文件夹，再保存一个快照B
> 	1. 回到系统刚装好的状态 - 快照A
> 	1. 还可再次回到快照B

## 虚拟机迁移删除

## VMTools

> VMTools 安装后，可以让我们在 Windows 下更好的管理 VM 虚拟机。
>
> 可以设置 Windows 和 CentOS 的共享文件夹。

### 安装步骤

1. 进入 CentOS；
2. 点击 VM 菜单中的 -> install vmware tools；
3. CentOS 会出现一个 VM 的安装包：xx.tar.gz；
4. 拷贝到 /opt；
5. 使用解压命令 tar，得到一个安装文件；
    tar -zxvf xx.tar.gz
6. 进入该 VM 解压目录 /opt 目录下；
    cd vmware..
7. 安装 ./vmware-install.pl；
8. 全部使用默认设置即可安装成功；

注意：
	安装 VMTools 需要 gcc
		gcc -v

<img src=".\image\vmtools_1.png" alt="vmtools_1" style="zoom: 33%;" />

### 设置共享文件夹

1. 菜单 -> vm -> setting，设置选项为 always enable；
2. Windows 和 CentOS 可共享 D:/share 目录，可进行读写文件了；
3. 共享文件夹在 CentOS 的 mnt/hgfs 目录下。

#### 注意事项与细节说明

1. Windows 和 CentOS 以上操作即可共享文件夹了，但*实际开发中*，文件的上传和下载是需要使用到==远程方式==来完成的。
2. ==远程方式==登录后面进行讲解。