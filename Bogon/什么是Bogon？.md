### 什么是Bogon？

bogon来源于bogon 空间的虚假 IP 地址。bogon是 Internet Assigned Number Authority (IANA) 或者 Regional Internet Registries ([RIR](https://www.ripe.net/participate/internet-governance/internet-technical-community/the-rir-system))未正式分配的IP地址集合。

Bogon IP 地址是合法地址。由于配置错误，您可能会看到一个 bogon IP 地址（无论是有意或无意）欺骗收件人关于发件人的合法 IP 地址。Bogon IP 地址在黑客或恶意活动中很流行，经常被用来发送垃圾邮件和发动分布式拒绝服务攻击。因此，许多 Internet 服务提供商和防火墙会封禁bogon。

Bogon有时指代bogon 空间，有时指代bogon IP地址。

## Techopedia对bogon的解释

IP地址是全世界互联网和内网基础设施最核心的组成部分。IP地址为网站、服务器或所有其他连网设备提供了唯一标识的方法。IP地址被用来实现客户端与应用程序之间的通信。IANA分配独一无二的IP地址给每个驻留在异构网络上的每个这样的实例和节点。分配或注册给任何实体的 IP 地址范围是 IP 地址保留空间的一部分。另一方面是，地址空间中没有注册过的任何其他地址是来自bogon空间。所有在bogon空间里的地址都被叫做bogon或者bogon IP地址。通常情况下，bogon在互联网或者所有计算机网络上都是不可见的。但这些bogon因为被用于非法或者欺诈犯罪，仍然被泄露了出来。黑客将源 IP 地址操纵为一个 bogon IP，使得接收方误以为包的来源可靠。

英文原文来自：https://www.techopedia.com/definition/2383/bogon