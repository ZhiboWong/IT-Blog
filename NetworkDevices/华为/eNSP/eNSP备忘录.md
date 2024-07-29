WiresharkPortable有过装了但是在eNSP无法使用的经历，建议使用完整版Wireshark。



环回网卡和虚拟网卡有何区别？为何eNSP的云设置虚拟网卡ping不通？



npcap不支持eNSP

FW的预置策略虽然是permit启用的，但是实际效果是所有方向的流量都阻拦。必须进编辑，确定后，才会生效。