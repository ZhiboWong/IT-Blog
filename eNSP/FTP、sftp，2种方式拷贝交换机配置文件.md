# FTP、sftp，2种方式拷贝交换机配置文件

## FTP

通过Windows自带的`ftp.exe` client，虽然可以连接上作为ftp server的SW，但是报错`200 PORT command successful`。This looks like a typical problem with the FTP active mode. The server cannot connect back to your machine to establish a data transfer connection.

See  article on [FTP modes and configuring network for the active mode](https://winscp.net/eng/docs/ftp_modes).

That typically happens as nowadays most client machines are behind a firewall or NAT or both, what prevents the FTP active mode from working. To make the active mode working you need to open your firewall (not recommended) and/or configure NAT routing rules.

Or you use the passive FTP mode. 但是`ftp.exe`只能采用主动模式，不支持被动模式，处处受限，所以`ftp.exe` 很鸡肋。客户端推荐使用第三方的ftp client。一开始用了xfile，但是连接不上服务器，报错。后来换成Xftp 7，完美运行。

## sftp

SFTP是SSH FTP的简称，一种安全的FTP。SFTP建立在SSH连接的基础之上，远程用户可以安全地登录设备，进行文件管理和文件传送等操作，为数据传输提供了更高的安全保障。

配置思路和stelnet类似。

## TFTP

其实有考虑过采用tftp，但是交换机不能作为tftp server，作罢。