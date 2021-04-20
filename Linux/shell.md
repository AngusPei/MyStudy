# Linux shell 命令备忘

## 挂载 NTFS 磁盘命令

**注意：** FAT32 格式不支持

```shell
diskutil list
sudo umount /dev/disk3s1 #卸载指定磁盘
sudo mount_ntfs -o rw,nobrowse /dev/disk3s1 ~/NTFS/ # 以可写方式挂载至~/NTFS/目录
```
