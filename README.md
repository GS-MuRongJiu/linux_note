# linux_note
一些常用的linux指令
## ls
显示所有文件及目录`a`
```shell
ls -a
```
![image](https://user-images.githubusercontent.com/127678470/230025196-9b562a1c-2ff7-4fc5-a91e-b9838d80ed97.png)

只显示目录`d`
```shell
ls -d
```
以长格式显示文件目录信息`l`
```shell
ls -l
```
![image](https://user-images.githubusercontent.com/127678470/230025468-128e79c9-8901-4616-8917-01f8a58a3d2a.png)


倒序显示文件目录`r`
```shell
ls -r
```
![image](https://user-images.githubusercontent.com/127678470/230025518-4035a59f-21a4-4977-adde-3ae881895f1a.png)

按照时间顺序排列文件目录`t`
```shell
ls -t
```
![image](https://user-images.githubusercontent.com/127678470/230025558-264ca775-8616-43a7-bd38-2424a6633d44.png)

不列出当前目录与父目录
```shell
ls -A
```
![image](https://user-images.githubusercontent.com/127678470/230025616-ffaccc4f-c499-4e4a-a904-5c3331a55168.png)

在列出的文件名称后加一符号；例如可执行档则加`*`, 目录则加`/`
```shell
ls -F
```
![image](https://user-images.githubusercontent.com/127678470/230025658-5ff749d8-359b-4df9-bdad-68b4f6c891a7.png)

递归显示目录中的所有文件和子目录
```shell
ls -R
```
![image](https://user-images.githubusercontent.com/127678470/230025701-7eeb6437-55b0-46f3-aed1-170a38995c2a.png)

##cd
返回home目录`~`
```shell
cd ~
```
![image](https://user-images.githubusercontent.com/127678470/230025830-f15ecebd-8e2e-4293-84f6-2f6d93f0172f.png)

`cd`后加目录路径跳转到相应目录
```shell
cd /bin
```
![image](https://user-images.githubusercontent.com/127678470/230025875-3752518f-8796-4255-a033-deea8c1a6dca.png)

## mv
为文件或目录改名、或将文件或目录移入其它位置
```shell
mv HomeWork Homework
```
![image](https://user-images.githubusercontent.com/127678470/230026052-2301b862-5f62-418f-a722-a429bb634718.png)

![image](https://user-images.githubusercontent.com/127678470/230026088-378731a9-0faf-4886-ac2a-4bdfdbe7ab8a.png)

将work1移动到Homework下
```shell
mv work1 Homework
```
![image](https://user-images.githubusercontent.com/127678470/230026143-43c92d16-8d23-43e3-ae69-b998e2e15ebb.png)

## pwd
显示当前目录
```shell
pwd
```
![image](https://user-images.githubusercontent.com/127678470/230026175-7444e2fc-8106-40bd-91c7-0cceeaa2dc89.png)

## rm
删除一个文件或者目录
```shell
rm work1
```
![image](https://user-images.githubusercontent.com/127678470/230026247-dd3c667a-a233-4160-b3ea-e46c5dcd5086.png)

删除目录
```shell
rm -r HomeWork
```
![image](https://user-images.githubusercontent.com/127678470/230026294-0db21925-6478-4b21-9aef-d84f03e501a6.png)

## cp
用于复制文件或目录
将`HomeWork`下的文件复制到`HomeWork2`中
```shell
cp -r /home/yang/HomeWork/* /home/yang/HomeWork2
```
![image](https://user-images.githubusercontent.com/127678470/230026539-7aad662a-eb96-4579-ba34-6c6e1a7c963a.png)

## tar
用于备份文件
## 程序前后台执行
程序前后台执行
```shell
gedit
```
![image](https://user-images.githubusercontent.com/127678470/230026610-be719dca-fafc-494a-9137-d5a50df6b10c.png)

前台调用文本编辑器后，终端无法使用

程序后台执行
```shell
gedit &
```
![image](https://user-images.githubusercontent.com/127678470/230026650-6a662761-5e95-4e83-bd71-db020209b2d6.png)

在命令后加&即可后台运行
 ## 使用`mount`来挂载设备
`mkdir /mnt/cdrom`将挂载源设备`/dev/cdrom`挂载到该挂载点`( /mnt/ cdrom)`上
`mount -t iso9660 -o ro / dev/cdrom /mnt/cdrom/`
`-t`:文件系统类型，iso9660表示光盘或者光盘镜像
`-o`:挂载方式，ro表示以只读方式，loop表示把挂载的设备当做一个磁盘分区
## 使用`env`查看环境变量
![image](https://user-images.githubusercontent.com/127678470/230026719-99eb7073-2e44-4a13-8d90-50e256bbf085.png)

## 使用`cat /etc/passwd`来查看用户信息文件
![image](https://user-images.githubusercontent.com/127678470/230026750-27ab2a63-b4aa-4d37-a12d-40cc425d3dd6.png)

## 使用`cast /proc/devices`查看设备加载信息文件
![image](https://user-images.githubusercontent.com/127678470/230026965-ee023fd7-f5ad-44b9-8c63-222ada88f585.png)

## 使用`netstat -ltnp`查看系统启动脚本文件
![image](https://user-images.githubusercontent.com/127678470/230027126-398244f9-6c15-459e-90fe-7e6d8c5fc3f8.png)

## Windows系统中的进程（用户进程与系统进程）和服务
服务：指系统自动完成的，不需要和用户交互的程序。
进程：程序运行的实例，系统会给运行中的进程分配CPU，内存等资源。
系统进程：用于完成操作系统的各种功能的进程就是系统进程
用户进程：由用户启动的进程就是用户进程

## windows命令
`copy`复制文件
区别：在linux中，既可以复制文件，也可以复制目录，但在windows中，只能复制文件，不能复制文件夹
`del`删除文件
区别：在linux中，既可以删除文件，也可以删除目录，但在windows中，只能删除文件，不能删除文件夹
`dir`显示目录的文件和子目录的列表

|参数	|描述|
|---|---|
|[<drive>:][<path>]	|指定要查看其列表的驱动器和目录|
|[<filename>]	|指定要查看其列表的特定文件或文件组。|
|/p	|一次显示一屏列表。要查看下一个屏幕，请按任意键。|
|/q	|显示文件所有权信息|
|/w	|以宽格式显示列表，每行最多包含五个文件名或目录名|
|/d	|以与 /w 相同的格式显示列表，但文件按列排序。|
|/a[[:]<attributes>]	|仅显示具有您指定属性的目录和文件的名称。|
|/o[[:]<sortorder>]	|根据 sortorder 对输出进行排序，它可以是以下值的任意组合：n - 按名称字母顺序排列排序顺序多个值按照您列出它们的顺序进行处理。不要用空格分隔多个值，但您可以选择使用冒号 |
|/t[[:]<timefield>]	|指定要显示或用于排序的时间字段。可用的时间字段值为：c - Creationa - 最后访问w - 最后写入|
|/s	|列出指定目录和所有子目录中指定文件名的每次出现。|
|/b	|显示目录和文件的裸列表，没有其他信息。 /b 参数覆盖 /w。|
|/l	|使用小写显示未排序的目录名和文件名。|
|/n	|在屏幕的最右侧显示带有文件名的长列表格式。|
|/x	|显示为非 8dot3 文件名生成的短名称。显示与 /n 的显示相同，但在长名称之前插入短名称。|
|/c	|以文件大小显示千位分隔符。这是默认行为。使用 /-c 隐藏分隔符。|
|/4	|以四位数格式显示年份。|
|/r	|显示文件的备用数据流。|
|/?	|在命令提示符处显示帮助。|
 
 与linux相比，`dir`支持更丰富的参数
 
 `cd`切换路径，可以通过在后面添加接驱动器符号、完整路径和相对路径来实现路径的转换 
|参数	|描述|
|---|---|
|/-|回到根目录|
|/..|回到上一目录|
|//d|进入相应目录|
|//?|查看帮助|
 
`cd`用法与linux中类似
 
 ## 配置环境变量
 将jdk放置在相应文件
 
 使用`tar -zxvf jdk-8u221-linux-x64.tar.gz`进行解压
 
 ## 修改环境变量
 输入`vi /etc/profile`进行配置
 
 点击`i`进入编辑模式，输入
 ```shell
 JAVA_HOME=/usr/local/java/jdk1.8.0_221
 CLASSPATH=%JAVA_HOME%/lib:%JAVA_HOME%/jre/lib
 PATH=$PATH:$JAVA_HOME/bin:$JAVA_HOME/jre/bin
 export PATH CLASSPATH JAVA_HOME
 ```
 
 输入指令`source /etc/profile`即可
 ## 添加用户
 `adduser`+用户名
 
 `passwd`+用户名设置密码
 
 `chown -R susu /liususu`更改目录所有者
 
 `chmod -R 755 /liususu`更改目录权限
 
