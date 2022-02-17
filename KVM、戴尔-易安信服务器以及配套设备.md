## KVM-over-IP Switches

> **Raritan provides a variety of KVM-over-IP Switches** that leverage today’s Ethernet and TCP/IP networks to provide anytime/anywhere remote access, control and management. Our Dominion KVM-over-IP switches provide at-the-rack access plus unlimited IP access and control via LAN, WAN and the Internet.
>
> 来源：Raritan

KVM-over-IP Switches可用于登陆机房服务器。

不支持两指滚屏操作。

| 具体OP         | 实质影响&其他                                  |
| -------------- | ---------------------------------------------- |
| 左键双击服务器 | 连接至服务器。有可能反应迟钝，双击间隔久一些。 |
| Fn + F12 双击  | 回到KVM-over-IP Switches主界面                 |



## DELL EMC

戴尔并购EMC（易安信）后，推出了戴尔EMC服务器。

![img](.assets/55b306d7-cd23-4b92-b43e-1502cfa5b84a.jpg)

<center>电源键在服务器面板右上方，绿灯代表正常工作</center>

| 具体OP       | 实质影响&其他 |
| ------------ | ------------- |
| Ctrl+Alt+Del | 重启服务器    |
|              |               |

### Power

![img](.assets/0b3a0ea0-a50c-4e1e-8b1f-c8724cfe067e.jpg)

![2kW](.assets/2kW.jpg)

![img](.assets/67b94333-6bee-4174-844c-ba28211de4a3.jpg)

![1.6kW](.assets/1.6kW.jpg)

此台服务器4电源，其中3块电源做冗余。实际上，一块电源就能够带动服务器运行。一般多块电池，都是做冗余，很少拿来做load balance。若想做load balance，在BIOS里可以更改。

### PCIe

![img](.assets/f5510678-4307-4dee-892b-e9770a092c00.jpg)

<center>PCIe集成内部</center>





![img](.assets/e6c1de26-f10a-444f-8458-270b59251e2a.jpg)

<center>PCIe集成外部</center>





![img](.assets/9e79b91c-51bf-4d29-b6af-a903049d172a.jpg)

<center>服务器后部缺失PCIe集成</center>

## 导轨

![img](.assets/58663e6a-9600-43fc-a598-48a4430a574c.jpg)

KVM-over-IP Switches控制台的导轨与服务器导轨类似，推进去时，需要把上图中的白色零件往里推，才能把导轨推进去。
