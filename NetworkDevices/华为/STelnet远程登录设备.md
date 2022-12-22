## 1、应用场景

Stelnet提供安全的认证方式，用户可以通过STelnet安全地登录远程设备，对设备进行管理和维护。

举个“栗子”
用户需要安全地登录远程设备，并对其进行方便地管理和维护：
设备作为SSH Server，IP地址为10.137.217.203/24。



## 2、前提条件

用户本地PC安装SSH服务器软件。本例中以PuTTY软件为例进行讲解。



## 3、配置思路

1、配置VTY用户界面。配置认证模式、协议。
2、创建SSH用户，并配置其认证方式为password认证。3步：密码、用户级别、服务协议，3者顺序不能颠倒，否则3者配不全。
3、使能STelnet服务器功能。
4、配置SSH用户的认证方式、服务方式。
5、用户在本地PC端通过STelnet方式登录SSH服务器。



### 4、操作步骤

```python
# 服务器端配置步骤
<HUAWEI> system-view 
[HUAWEI] sysname SSH Server 
[SSH Server] user-interface vty 0 4 #vty虚拟类型###(Virtual Type)终端统一配置0-4，五个用户
[SSH Server-ui-vty0-4] authentication-mode aaa 
[SSH Server-ui-vty0-4] protocol inbound ssh 
[SSH Server-ui-vty0-4] quit
[SSH Server] aaa 
[SSH Server-aaa] local-user client001 password cipher Huawei@123 #创建SSH用户client001(名字可变)并配置其认证方式为cipher.账户密码是在aaa视图创建按。
[SSH Server-aaa] local-user client001 privilege level 3 #指定用户级别。
[SSH Server-aaa] local-user client001 service-type ssh #设置服务类型为ssh
[SSH Server-aaa] quit 
[SSH Server] stelnet server enable	#开启STelnet服务器功能
[SSH Server] ssh user client001 authentication-type password #配置SSH用户的认证方式
[SSH Server] ssh user client001 service-type stelnet	#配置SSH用户的服务方式。若是路由器，无需配置这条命令。

若是较新版本的SW，还需要配置ssh server-source all-interface。
因为即默认情况下，交换机中存在着以下命令：
  undo ssh server-source all-interface
  此条命令的意思为，交换机的所有接口拒绝SSH登陆；

# 之后配置本地PC的PuTTY或者CRT软件参数，远程连接设备
```



#### 关于用户级别

整数形式，取值范围是0～15。取值越大，级别越高。缺省情况下，命令级别分为0～3级：

- 级别0即参观级，包括网络诊断工具命令（ping、tracert）、从本设备出发访问外部设备的命令（例如Telnet）等。该级别命令不允许进行配置文件保存的操作。
- 级别1即监控级，用于系统维护，包括display命令。该级别命令不允许进行配置文件保存的操作。
- 级别2即配置级，可以使用业务配置命令，包括路由、各个网络层次的命令，向用户提供直接网络服务。
- 级别3即管理级，用于系统基本运行的命令，对业务提供支撑作用，包括文件系统、FTP、TFTP、配置文件切换命令、备板控制命令、用户管理命令、命令级别设置命令；用于业务故障诊断的debugging命令。