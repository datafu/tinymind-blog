---
title: VMWare  挂载新虚拟磁盘
date: 2024-09-22T10:13:32.614Z
---


虚拟磁盘的使用步骤
创建虚拟磁盘：
在 VMware 或其他虚拟化软件中创建新的虚拟磁盘。
启动虚拟机：
启动包含新虚拟磁盘的 Red Hat 虚拟机。
识别新磁盘：
使用以下命令查看新磁盘：

   fdisk -l



二、创建分区（如果需要）
如果新磁盘没有分区，可以使用 fdisk 工具进行分区：
sudo fdisk /dev/sdb：进入分区工具。
输入 n 创建新分区，选择分区类型（通常选择主分区 p），设置分区编号、起始扇区和结束扇区等，可使用默认值，最后输入 w 保存分区表。

分区和格式化：
使用 fdisk 或 parted 创建分区，并使用 mkfs 格式化

sudo mkfs.ext4 /dev/sdb1

挂载虚拟磁盘：

创建挂载点并挂载磁盘：

sudo mkdir /mnt/newdisk
sudo mount /dev/sdb1 /mnt/newdisk

自动挂载（可选）：
若要在系统启动时自动挂载，请编辑 /etc/fstab 文件，添加相应的挂载信息。

/dev/sdb1  /mnt/newdisk  ext4  defaults  0  0

