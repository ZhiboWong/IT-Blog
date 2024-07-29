```shell







## 2、常用命令：

gawk -- Gnu AWK

mawk -- Minimal AWK

grep -- General Regular Expression Println -- LiNktar -- TARball

#### 查找指定文件||file

##### find  



##### locate

`locate` 命令比 `find` 命令运行得更快，因为它使用 `updatedb` 数据库，而 `find` 命令在真实系统中搜索。

它使用数据库而不是搜索单个目录路径来获取给定文件。

`locate` 命令未在大多数发行版中预安装，因此，请使用你的包管理器进行安装。

```bash
$ sudo updatedb`
```

##### which

只能查找\usr下的

##### whereis



### 2.2、硬件管理：

df -- Disk Free

du -- Disk Usage

dd -- Data Description（有说是Convert and Copy， 但是cc被用掉了，就用dd了）

parted -- PARTition EDitor

fdisk -- Format DISK		
sudo fdisk --list,    sudo fdisk -l,查看硬盘分区表

lspci -- LiSt Peripheral Component Interconnectlscpu -- LiSt Central Process Unit

lsusb -- LiSt Universal Serial Bus

lsblk -- LiSt BLocK,查看磁盘情况

mdadm -- Multiple Disk And Device Manager

#### 2.2.1、

lvmlvm -- Logical Volume Manager

pvcreate -- Physical Volume CREATE

vgcreate -- Volume Group CREATE

lvcreate -- Logical Volume CREATE

pvdisplay -- Physical Volume DISPLAY

vgdisplay -- Volume Group DISPLAY

lvdisplay -- Logical Volume DISPLAY

pvresize -- Physical Volume RESIZE

vgresize -- Volume Group RESIZE

lvresize -- Logical Volume RESIZE

pvextend -- Physical Volume EXTENDvgextend -- Volume Group EXTENDlvextend -- Logical Volume EXTENDpvremove -- Physical Volume REMOVEvgremove -- Volume Group REMOVElvremove -- Logical Volume REMOVEpvs -- Physical Volume Statusvgs -- Volume Group Statuslvs -- Logical Volume Status

### 2.3、软件及软件包管理：

man -- MANual

apt -- Advanced Packaging Tool

dpkg -- Debian PacKaGe

yum -- Yellow dog Updater Modified

rpm -- Redhat Package Manager包管理工具

### 2.4、用户及用户组管理：

useradd -- USER Add

userdel -- USER DELete

usermod -- USER MODify

users -- USER Status

groupadd -- GROUP ADD

groupdel -- GROUP DELete

groupmod -- GROUP MODify

groupmems -- GROUP MEMberS
sudo su    提权
### 2.5、系统管理：

init 6	#reboot

depmod -- DEPend MODule

hostname	查看当前用户名	

lsmod -- LiSt MODule

modprobe -- MODule PROBE

modinfo -- MODule INFOrmation

insmod -- INSert MODule

rmmod -- ReMove MODule

mkfs -- MaKe FileSystem

fsck -- File System Consistency Check


su -- Substitute User|| Switch User更换用户

bash -- Bourne Again SHell

dash -- Debian Almquist SHellinit -- INITialization

ssh -- Secure SHell

wine -- Wine Is Not an Emulator

exec -- EXECute

fstab -- FileSystem TABle

passwd -- PASSWorD

chpasswd -- CHange PASSWorD

pwconv -- PassWord CONVert

pwunconv -- PassWord UNCONVert

tty -- TeleTYpe

sudo -- SuperUser DO

grub -- GRand Unified Bootloader

tzselect -- Time Zone SELECT

sync -- SYNChronize

systemd -- SYSTEM Daemon (里面有systemctl bootctl journalctl loginctl localectl timedatectl 等等，都是blablabla ConTroL）

### 2.6、编辑器：

ed -- EDitor

nano -- Nano's ANOther 

editoremacs -- Editor MACroS（还有很多全称，就不罗列了，这个接受度比较广）

vi -- VIsual

vim -- Vi Improved

### 2.7、编译器：

cc -- C Compiler

gcc -- Gnu Compiler Collection（作为一个软件集被你下载下来编译安装的时候）

g++ -- Gnu c++ compiler

gcj -- Gnu Compiler for Java

yacc -- Yet Another Compiler Compiler

guile -- Gnu Ubiquitous Intelligent Language for Extensions

gas -- Gnu Assembler

php -- PHP：Hypertext Preprocessor

ld -- LoaD

gdb -- Gnu DeBug

tcl -- Tool Command Line

## 3、图形界面：

gnome -- GNu Object Model Environment

gdm -- Gnome Display Managergtk -- Graphic user interface ToolKitqt -- ………………Toolkit（不说Q了，用Q只是因为在开发者的Emacs中Q特别漂亮…………）kde -- K Desktop Environmentlxde -- Lightweight X11 Desktop Environmentxfce -- XForms Common Environment

### 4、参数

（声明：只是通常会使用的参数，并不一定是通用参数，使用时请注意）：-h | --help：help-v | --version：version（吐槽一下java）

### 5、许可证

gnu gpl : Gnu General Public License

gnu lgpl : Gnu  Lesser General Public License GNU通用公共许可证

gfdl : Gnu Free Documentation License

agpl : Affero General Public License（或简写为Affero gpl)apsl : Apple Public Source Licensebsd : Berkeley Software Distribution license

​		

