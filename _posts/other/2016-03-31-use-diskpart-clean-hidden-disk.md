---
layout: post
title:  "u盘影藏分区恢复"
author: runphp
date:   2016-03-31 00:07:12 +0800
category: other
tags: diskpart
---
环境windows10

命令提示符(管理员)

{% highlight bash %}
C:\WINDOWS\system32>diskpart

Microsoft DiskPart 版本 10.0.10240

Copyright (C) 1999-2013 Microsoft Corporation.
在计算机上: HEHUI-PC

DISKPART> list disk

  磁盘 ###  状态           大小     可用     Dyn  Gpt
  --------  -------------  -------  -------  ---  ---
  磁盘 0    联机              111 GB  1024 KB
  磁盘 1    联机              931 GB  1024 KB
  磁盘 2    联机             7651 MB      0 B

DISKPART> select disk 2

磁盘 2 现在是所选磁盘。

DISKPART> clean

DiskPart 成功地清除了磁盘。

DISKPART> create partition primary

DiskPart 成功地创建了指定分区。

DISKPART> select partition 1

分区 1 现在是所选分区。

DISKPART> format quick fs=ntfs

  100 百分比已完成

DiskPart 成功格式化该卷。

DISKPART> assign

DiskPart 成功地分配了驱动器号或装载点。

DISKPART> exit
{% endhighlight %}
