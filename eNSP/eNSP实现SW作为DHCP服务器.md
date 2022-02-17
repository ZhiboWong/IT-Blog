### DHCP服务器配置

```
#vlanif接口下需配置ip地址
interface Vlanif10
 ip address 192.168.10.1 255.255.255.0
 dhcp select global 					#用来开启接口采用全局地址池的DHCP Server功能。
```

```
#系统视图下
dhcp enable
```

```
ip pool dhcp10	#创建地址池，之后进入IP地址池视图
 gateway-list 192.168.10.1	#设置网关
 network 192.168.10.0 mask 255.255.255.0	#设置ip地址段
```

