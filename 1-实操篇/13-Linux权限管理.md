[toc]

# 权限

## 基本介绍

当使用 ll 时，显示：
-rwxrw-r-- 1 root root 1213 Feb 2 09:39 abc

### 说明

- 第 0 位，确定文件的类型(- l d c b)
    - -：文件。
    - l：链接。相当于 Windows 的快捷方式。
    - d：目录。相当于 Windows 的文件夹。
    - c：字符设备文件。如：鼠标，键盘。
    - b：块设备。如：硬盘。
- 第 1-3 位，确定所有者(user)拥有该文件的权限。
- 第 4-6 位，确定所属组(group)拥有该文件的权限。
- 第 1-3 位，确定其他用户(other)拥有该文件的权限。

# rwx 权限

## rwx 作用到文件

1. r [read]：可以读取，查看。
2. w [write]：可以修改，但不代表可以删除该文件。
3. x [execute]：可以被执行。

## rwx 作用到目录

1. r [read]：可以读取，ls 查看目录内容。
2. w [write]：可以修改，对目录内创建 / 删除 / 重命名目录。
3. x [execute]：可以进入该目录。

# 修改权限

## chmod

### 基本说明

> 通过 chmod 指令，可以修改文件或者目录的权限。

### 方式一

> 第一种方式：
> 	+、-、= 变更权限。
> 	u：所有者	g：所属组	o：其他人	a：所有人
>
> chmod u=rwx,g=rx,o=x 文件 / 目录名
>
> chmod o+w 文件 / 目录名
>
> chmod a-x 文件 / 目录名

> 第二种方式：
> 	通过数字变更权限。
> 	r = 4，w = 2，x = 1

## chown

> chown newowner 文件 / 目录 
> 	改变文件 / 目录的所有者。
>
> chown newowner:newgroup 文件 /目录
> 	改变文件 /目录的所有者和所属组。
>
> chown -R newowner:newgroup 文件 /目录
> 	如果是目录，则使其下所有子文件或目录递归生效。

## chfrp

> chgrp newgroup 文件 / 目录
> 	改变所属组。

