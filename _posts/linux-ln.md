## linux ln 命令学习

### 链接文件
ln -s abc def 建立abc的软链接为def
ln abc def  建立abc的硬链接为def

### 软链接文件夹
ln -s abc/ def 建立abc目录的软连接为def

### 删除软链接
rm abc 删除软链接

### 软硬链接的区别
1. 软链接可以跨文件系统，硬链接不可以
2. 硬链接节点数随着链接数增多而增多，只要硬链接数不为0，文件一直存在
   软链接删除对源文件没有影响,删除源文件，软连接文件索引不到
3. 软链接可以对一个不存在的文件进行链接
4. 软链接可以对目录进行链接
