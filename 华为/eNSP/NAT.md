首先要说的是，要在出口路由器 or FW上写去程路由&回程路由。

## 静态NAT

```python

[Huawei]ip route-static 10.1.2.0 24 192.168.1.3
[Huawei]nat static global 192.168.1.2 inside 10.1.1.2 #可以在系统视图下输入，也可以在接口视图下输入
```



## 动态NAT

```c
[R1]nat address-group 1 202.1.1.1 202.1.1.1     //定义一个地址池1存放一个共用的公网地址202.1.1.1
[R1]acl 2000
[R1-acl-basic-2000]rule 5 per source 192.168.1.0 0.0.0.255      //定义ACL允许进行NAT转换的源ip
[R1-acl-basic-2000]int g0/0/1
[R1-GigabitEthernet0/0/1]ip add 202.106.1.2 30
[R1-GigabitEthernet0/0/1]nat outbound 2000 address-group 1      //在出口下将ACL和地址池关联起来，需要注意华为设备上如果地址池中有不止一个ip地址，后面需加no-pat，本例中因只有一个地址池可以不加
```

`no-pat`是不使用端口的意思，即每次数据包的发送源地址不一样。通过源端口号区分不同数据包。

不加`no-pat`，就是一个内网地址使用地址池中的一个外网地址，源IP一样，但是每个数据包的源端口号不一样。通过源IP区分不同的数据包。



## Easy IP

```c
[R1]acl 2000
[R1-acl-basic-2000]rule 5 per source 192.168.1.0 0.0.0.255  //定义ACL允许进行NAT转换的源IP。5是代表第5条acl规则。若不输入规则号，默认规则号从5开始计数，步长为5。
[R1-acl-basic-2000]int g0/0/1
[R1-GigabitEthernet0/0/1]nat outbound 2000      //定义复用接口g0/0/1用于PAT转换。PAT也叫做PNAT，基于Port(端口)的NAT。
```



另外，有时候配置明明是对的，但是就是不通。有可能是模拟器的问题，重启模拟器试试看。