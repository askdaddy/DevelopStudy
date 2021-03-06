linux文件权限
===

###（一）查看文件权限命令
在终端输入ls -l xxx.xxx （xxx.xxx是文件名）会显示
-rwxr-xr-x

###（二）文件权限说明
文件权限实例：-rwxr-xr-x  
一共有10位数  
其中： 最前面那个 - 代表的是类型  
2-4位  rwx 代表的是所有者（user）  
5-7位  r-x 代表的是组群（group）  
8-10位 r-x 代表的是其他人（other） 

**符号定义：**  
r 表示文件可以被读（read）  
w 表示文件可以被写（write）  
x 表示文件可以被执行（如果它是程序的话）  
- 表示相应的权限还没有被授予  
rwx也可以用数字来代替  
r 4  
w 2  
x 1  
- 0  

**范例分析：**  
-rw------- (600) 只有所有者才有读和写的权限  
-rwx------ (700) 只有所有者才有读，写，执行的权限  
-rwx--x--x (711) 只有所有者才有读，写，执行的权限，组群和其他人只有执行的权限  
-rw-rw-rw- (666) 每个人都有读写的权限  
-rwxrwxrwx (777) 每个人都有读写和执行的权限  

###（三）修改文件权限命令
在终端输入chmod 664 a.txt  
可以修改 a.txt 文件权限为-rw-rw-r--

修改整个文件夹里面文件权限的命令  
chmod -R 777 ./bin

###（四）toy：双击脚本运行其他脚本
有时候为了运行一个脚本，得打开终端跳到当前目录，执行对应脚本，繁琐，所以写个简单的脚本run.sh，用来直接运行当前目录指定的脚本。  
run.sh内容如下：

	gnome-terminal -t "title-name" -x bash -c "sh ./order.sh;exec bash;"
-t 为打开终端的标题，便于区分。  
-x 后面的为要在打开的终端中执行的脚本，根据需要自己修改就行了。  
exec bash;是让打开的终端在执行完脚本后不关闭。  

先通过终端运行chmod 777 run.sh将run.sh设置为可执行文件，在当前目录增加 order.sh 待执行的脚本文件，双击运行run.sh即可。

mac 系统和 linux 不同，mac 系统适配版：  
1.无gnome-terminal命令，命令改成open -a Terminal.app order.sh  
2.运行方式：右键 run.sh 打开方式选择其他-》实用工具-》终端  
其实也可以直接采用2运行方式直接运行 order.sh