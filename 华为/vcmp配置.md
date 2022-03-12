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

