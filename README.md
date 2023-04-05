# linux_note
一些常用的linux指令
## ls
显示所有文件及目录`a`
```shell
ls -a
```
只显示目录`d`
```shell
ls -d
```
以长格式显示文件目录信息`l`
```shell
ls -l
```
倒序显示文件目录`r`
```shell
ls -r
```
按照时间顺序排列文件目录`t`
```shell
ls -t
```
不列出当前目录与父目录
```shell
ls -A
```
在列出的文件名称后加一符号；例如可执行档则加`*`, 目录则加`/`
```shell
ls -F
```

递归显示目录中的所有文件和子目录
```shell
ls -R
```
##cd
返回home目录`~`
```shell
cd ~
```
`cd`后加目录路径跳转到相应目录
```shell
cd /bin
```
## mv
为文件或目录改名、或将文件或目录移入其它位置
```shell
mv HomeWork Homework
```
将work1移动到Homework下
```shell
mv work1 Homework
```
## pwd
显示当前目录
```shell
pwd
```
## rm
删除一个文件或者目录
```shell
rm work1
```
删除目录
```shell
rm -r HomeWork
```
## cp
用于复制文件或目录
将`HomeWork`下的文件复制到`HomeWork2`中
```shell
cp -r /home/yang/HomeWork/* /home/yang/HomeWork2
```
## tar
用于备份文件
## 程序前后台执行
程序前后台执行
```shell
gedit
```
前台调用文本编辑器后，终端无法使用

程序后台执行
```shell
gedit &
```
在命令后加&即可后台运行
 ## 使用`mount`来挂载设备
`mkdir /mnt/cdrom`将挂载源设备`/dev/cdrom`挂载到该挂载点`( /mnt/ cdrom)`上
`mount -t iso9660 -o ro / dev/cdrom /mnt/cdrom/`
`-t`:文件系统类型，iso9660表示光盘或者光盘镜像
`-o`:挂载方式，ro表示以只读方式，loop表示把挂载的设备当做一个磁盘分区
## 使用`env`查看环境变量

## 使用cat /etc/passwd来查看用户信息文件

## 设备挂载信息文件
查看内核/操作系统/CPU信息`uname -a`
查看操作系统版本 `head -n 1 /etc/issue`
查看CPU信息`cat/proc/cpuinfo`
