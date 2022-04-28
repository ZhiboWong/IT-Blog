首先要保证SW之间可以通信，才能配置VCMP

### Server

```
vcmp role server
[AGG] vcmp domain vd1 
[AGG] vcmp device-id server 
[AGG] vcmp authentication sha2-256 password P@ssw0rd

```

### Client

```
[ACC2] vcmp domain vd1 
[ACC2] vcmp authentication sha2-256 password P@ssw0rd
```



vcmp客户端密码错误不会提示。若想验证密码是否正确，只需要在server创立一个vlan，紧接着在client看看vlan有没有跟随创建，即可判断client上的vcmp密码是否正确。

